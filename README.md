# RXL-RADSet

![RXL-RADSet](https://img.shields.io/badge/Dataset-RXL--RADSet-blue)
![License](https://img.shields.io/badge/License-CC--BY--NC--SA%204.0-lightgrey)

# **RXL-RADSet: A Radiologist-Validated Synthetic Benchmark for Language Models**

[Kartik Bose](mailto:0xkbose@pm.me)<sup>1</sup>, Raghuraman Soundararajan<sup>1</sup>, Abhinandan Kumar<sup>1</sup>, Priya Mudgil<sup>1</sup>, Samonee Ralmilay<sup>1</sup>, Niharika Dutta<sup>1</sup>, Manphool Singhal<sup>1</sup>, Arun Sharma<sup>1</sup>, Saugata Sen<sup>2</sup>, Anurima Patra<sup>2</sup>, Priya Gosh<sup>2</sup>, Abanti Das<sup>3</sup>, Amit Gupta<sup>4</sup>, Ashish Verma<sup>5</sup>, Dipin Sudhakaran<sup>6</sup>, Ekta Dhamija<sup>7</sup>, Himangi Unde<sup>8</sup>, Ishan Kumar<sup>5</sup>, Krithika Rangarajan<sup>7</sup>, Prerna Garg<sup>9</sup>, Rachel Sequeira<sup>8</sup>, Sudhin Shylendran<sup>10</sup>, Taruna Yadav<sup>11</sup>, Tej Pal<sup>4</sup>, <sup>*</sup>[Pankaj Gupta](mailto:pankajgupta959@gmail.com)<sup>1</sup>, 

<sup>1</sup> Department of Radiodiagnosis, Postgraduate Institute of Medical Education and Research, Chandigarh, India 160012
<br><sup>2</sup> Department of Radiodiagnosis, Tata Medical Center, Kolkata, India 700156
<br><sup>3</sup> Department of Radiodiagnosis, All India Institute of Medical Sciences, Kalyani, India 741245
<br><sup>4</sup> Department of Radiodiagnosis, National Cancer Institute, Jhajjar, India 124105
<br><sup>5</sup> Department of Radiodiagnosis, Banaras Hindu University, Varanasi, India 221005
<br><sup>6</sup> Department of Radiodiagnosis, Aster Malabar Institute of Medical Sciences, Kerala, India 670621
<br><sup>7</sup> Department of Radiodiagnosis, All India Institute of Medical Sciences, New Delhi, India 110029
<br><sup>8</sup> Department of Radiodiagnosis, Tata Main Hospital, Mumbai, India, 400012
<br><sup>9</sup> Department of Radiodiagnosis, Rajiv Gandhi Cancer Institute and Research Centre, Delhi, India 110085
<br><sup>10</sup> Department of Radiodiagnosis, Baby Memorial Hospital, Kerala, India 670621
<sup>11</sup> Department of Radiodiagnosis, All India Institute of Medical Sciences, Jodhpur, India 342005
**<br><sup>*</sup>Corresponding Author**

![RXL-RADSet Overview](assets/images/dataset_overview.png)

---

## About the Dataset

**RXL-RADSet** is a comprehensive benchmark dataset designed for evaluating language models on radiology report understanding and generation tasks.

### Key Features

- **Radiologist-Validated**: All reports have been validated by experienced radiologists
- **Synthetic Generation**: Reports are generated using controlled synthetic methods ensuring quality and diversity
- **Multi-Modal Coverage**: Includes reports across CT, MRI, Mammography, and Ultrasound
- **10 RADS Systems**: Covers NI-RADS, TI-RADS, Lung-RADS, BI-RADS, CAD-RADS, LI-RADS, GB-RADS, VI-RADS, PI-RADS, and O-RADS

### Purpose

This dataset aims to advance research in medical language models by providing a high-quality, standardized benchmark for tasks such as:
- Report generation
- Clinical finding extraction
- Impression generation
- Report classification

---

## Dataset Characteristics

| Characteristic | Value |
|----------------|-------|
| **Total Reports** | 1,600 |
| **Number of RADS Systems** | 10 |
| **Modalities Covered** | CT, MRI, Mammography, Ultrasound |

### Dataset Distribution by Modality

| Domain    | CT  | MRI | Mammography | Ultrasound | Total |
| --------- | --- | --- | ----------- | ---------- | ----- |
| BI-RADS   | 0   | 100 | 100         | 100        | 300   |
| CAD-RADS  | 100 | 0   | 0           | 0          | 100   |
| GB-RADS   | 0   | 0   | 0           | 100        | 100   |
| LI-RADS   | 150 | 150 | 0           | 100        | 400   |
| Lung-RADS | 100 | 0   | 0           | 0          | 100   |
| NI-RADS   | 100 | 0   | 0           | 0          | 100   |
| O-RADS    | 0   | 100 | 0           | 100        | 200   |
| PI-RADS   | 0   | 100 | 0           | 0          | 100   |
| TI-RADS   | 0   | 0   | 0           | 100        | 100   |
| VI-RADS   | 0   | 100 | 0           | 0          | 100   |

### RADS Score Distribution

| **RADS**         | **N**  | **0** | **1** | **2** | **2a** | **2b** | **3**  | **4** | **4A** | **4B** | **4C** | **5**  | **6** | **Equivocal** | **M** | **N** | **NC** | **TIV** | **V** |
| --------------- | ----- | ----- | ----- | ----- | ------ | ------ | ------ | ----- | ------ | ------ | ------ | ------ | ----- | ------------- | ----- | ----- | ------ | ------- | ---- |
| BI-RADS         | 300   | 9     | 31    | 75    |        |        | 50     | 33    | 15     | 23     | 8      | 31     | 25    |               |       |       |        |         |      |
| CAD-RADS        | 100   | 29    | 15    | 22    |        |        | 19     |       | 7      | 5      |        | 2      |       |               | 1     |       |        |         |      |
| GB-RADS         | 100   | 8     | 29    | 33    |        |        | 14     | 6     |        |        |        | 10     |       |               |       |       |        |         |      |
| LI-RADS         | 300   |       | 73    | 40    |        |        | 106    | 6     |        |        |        | 68     |       | 5             |       |       |        | 2       |      |
| *LR-TR           | 100   |       |       |       |        |        |        |       | 2      |        | 1      | 14     | 63    |               | 20    |       |        |         |      |
| NI-RADS | 100  |       | 55    | 1     | 4      | 1      | 38     | 1     |        |        |        |        |       |               |       |       |        |         |      |
| O-RADS          | 200   | 3     | 4     | 88    |        |        | 47     | 17    |        |        |        | 41     |       |               |       |       |        |         |      |
| PI-RADS         | 100   |       | 14    | 10    |        |        | 19     | 25    |        |        |        | 32     |       |               |       |       |        |         |      |
| TI-RADS         | 100   |       | 3     | 12    |        |        | 15     | 22    |        |        |        | 33     |       |               |       | 15    |        |         |      |
| Lung-RADS       | 100   |       | 34    | 27    |        |        | 9      | 4     | 10     | 16     |        |        |       |               |       |       |        |         |      |
| VI-RADS         | 100   |       | 9     | 28    |        |        | 14     | 21    |        |        |        | 21     |       |               |       | 7     |        |         |      |

<sup>*LI-RADS includes LR-TR (100) which is mentioned in a separate row.</sup>

---

## Sample Reports

Below are representative samples from the RXL-RADSet dataset. Click on any report to view the full PDF.

### LI-RADS Samples

| Report | Modality | Profile | RADS Score |
|--------|----------|---------|------------|
| [R038_L_MRI.pdf](assets/samples/LI-RADS/MRI/R038_L_MRI.pdf) | MRI | 3 | 3 |
| [R095_L_CT.pdf](assets/samples/LI-RADS/CT/R095_L_CT.pdf) | CT | 2 | LR-TR 5 |

### O-RADS Samples

| Report | Modality | Profile | RADS Score |
|--------|----------|---------|------------|
| [R013_O_MRI.pdf](assets/samples/O-RADS/MRI/R013_O_MRI.pdf) | MRI | 4 | 3 |
| [R076_O_US.pdf](assets/samples/O-RADS/US/R076_O_US.pdf) | Ultrasound | 2 | 4 |

### PI-RADS Samples

| Report | Modality | Profile | RADS Score |
|--------|----------|---------|------------|
| [R065_P_MRI.pdf](assets/samples/PI-RADS/R065_P_MRI.pdf) | MRI | 5 | 4 |

### Metadata

The complete dataset includes a metadata file with standardized information for each report:

```csv
Report_Number,Modality,Profile,RADS_score
R001_B_MG,Mammography,1,1
R002_B_MG,Mammography,1,0
R003_B_MG,Mammography,1,2
...
```

**Metadata fields:**
- `Report_Number`: Unique identifier (e.g., R001_B_MG = Report 1, BI-RADS, Mammography)
- `Modality`: Imaging modality (CT, MRI, Mammography, Ultrasound)
- `Profile`: Radiologist profile used (1-5)
- `RADS_score`: Assigned RADS score

The full metadata file is available at [`assets/samples/metadata.csv`](assets/samples/metadata.csv).

---

## Dataset Access

To request access to the RXL-RADSet dataset, please complete the following form:

[**Request Dataset Access**](https://docs.google.com/forms/d/e/1FAIpQLSeOXcp63Fhe2Vlmm1FiuBuABejkgj_Y7HSlt-bMMw7klkWB3Q/viewform?usp=publish-editor)

### Access Process

1. Complete the access request form with your institutional details
2. Specify your intended use case for the dataset
3. Agree to the dataset license terms (CC BY-NC-SA 4.0)
4. You will receive download instructions via email
<!-- TODO: Uncomment and add timeline
within **X business days**
-->

---

## Citation

If you use RXL-RADSet in your research, please cite:

```bibtex
@dataset{rxl_radset2025,
  title={RXL-RADSet: A Radiologist-Validated Synthetic Benchmark for Language Models},
  author={Pankaj Gupta, Kartik Bose},
  year={2025},
  publisher={arXiv},
  url={https://github.com/yourusername/RADSet}
}
```

<!-- TODO: Add link to paper if available
**Paper:** [Link to paper](URL)
-->

---

## License

This dataset is licensed under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)**.

- [![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

You are free to:
- **Share**: Copy and redistribute the material in any medium or format
- **Adapt**: Remix, transform, and build upon the material

Under the following terms:
- **Attribution**: You must give appropriate credit
- **NonCommercial**: You may not use the material for commercial purposes
- **ShareAlike**: If you remix, transform, or build upon the material, you must distribute your contributions under the same license

---

## Contact

For questions about the dataset, access requests, or collaboration opportunities, [please email us by clicking here](mailto:0xkbose@pm.me?cc=pankajgupta959@gmail.com)

---

<!-- TODO: Uncomment and add acknowledgments
## Acknowledgments
-->
