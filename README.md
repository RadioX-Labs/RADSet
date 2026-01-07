# RXL-RADSet

![RXL-RADSet](https://img.shields.io/badge/Dataset-RXL--RADSet-blue)
![License](https://img.shields.io/badge/License-CC--BY--NC--SA%204.0-lightgrey)

### RXL-RADSet: A Radiologist-Validated Synthetic Benchmark for Language Models

[Kartik Bose](mailto:0xkbose@pm.me)<sup>1</sup>, Raghuraman Soundararajan<sup>1</sup>, Abhinandan Kumar<sup>1</sup>, Priya Mudgil<sup>1</sup>, Samonee Ralmilay<sup>1</sup>, Niharika Dutta<sup>1</sup>, Manphool Singhal<sup>1</sup>, Arun Sharma<sup>1</sup>, Saugata Sen<sup>2</sup>, Anurima Patra<sup>2</sup>, Priya Gosh<sup>2</sup>, Abanti Das<sup>3</sup>, Amit Gupta<sup>4</sup>, Ashish Verma<sup>5</sup>, Dipin Sudhakaran<sup>6</sup>, Ekta Dhamija<sup>7</sup>, Himangi Unde<sup>8</sup>, Ishan Kumar<sup>5</sup>, Krithika Rangarajan<sup>7</sup>, Prerna Garg<sup>9</sup>, Rachel Sequeira<sup>8</sup>, Sudhin Shylendran<sup>10</sup>, Taruna Yadav<sup>11</sup>, Tej Pal<sup>4</sup>, <sup>*</sup>[Pankaj Gupta](mailto:pankajgupta959@gmail.com)<sup>1</sup>, 

<sup>1 Department of Radiodiagnosis, Postgraduate Institute of Medical Education and Research, Chandigarh, India 160012</sup>
<br><sup>2 Department of Radiodiagnosis, Tata Medical Center, Kolkata, India 700156</sup>
<br><sup>3 Department of Radiodiagnosis, All India Institute of Medical Sciences, Kalyani, India 741245</sup>
<br><sup>4 Department of Radiodiagnosis, National Cancer Institute, Jhajjar, India 124105</sup>
<br><sup>5 Department of Radiodiagnosis, Banaras Hindu University, Varanasi, India 221005</sup>
<br><sup>6 Department of Radiodiagnosis, Aster Malabar Institute of Medical Sciences, Kerala, India 670621</sup>
<br><sup>7 Department of Radiodiagnosis, All India Institute of Medical Sciences, New Delhi, India 110029</sup>
<br><sup>8 Department of Radiodiagnosis, Tata Main Hospital, Mumbai, India, 400012</sup>
<br><sup>9 Department of Radiodiagnosis, Rajiv Gandhi Cancer Institute and Research Centre, Delhi, India 110085</sup>
<br><sup>10 Department of Radiodiagnosis, Baby Memorial Hospital, Kerala, India 670621</sup>
<sup>11 Department of Radiodiagnosis, All India Institute of Medical Sciences, Jodhpur, India 342005</sup>
**<br><sup>* Corresponding Author**</sup>

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

| RADS      | N   | Modality | 0   | 1   | 2   | 2A  | 2B  | 3   | 4   | 4A  | 4B  | 4C  | 5   | 6   | E   | M   | N   | NP  | NV  | TIV | V   |
| --------- | --- | -------- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| BI-RADS   | 100 | MRI      | 0   | 9   | 23  | 0   | 0   | 16  | 19  | 0   | 0   | 0   | 13  | 20  | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| BI-RADS   | 100 | US       | 0   | 3   | 32  | 0   | 0   | 25  | 0   | 7   | 12  | 8   | 13  | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| BI-RADS   | 100 | Mammo    | 9   | 19  | 19  | 0   | 0   | 10  | 14  | 7   | 12  | 0   | 5   | 5   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| GB-RADS   | 100 | US       | 8   | 29  | 33  | 0   | 0   | 14  | 6   | 0   | 0   | 0   | 10  | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| LI-RADS   | 100 | CT       | 0   | 17  | 5   | 0   | 0   | 37  | 3   | 0   | 0   | 0   | 34  | 0   | 0   | 2   | 0   | 0   | 0   | 2   | 0   |
| LI-RADS   | 100 | CT/MRI   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 1   | 0   | 1   | 14  | 63  | 0   | 21  |
| LI-RADS   | 100 | MRI      | 0   | 25  | 5   | 0   | 0   | 30  | 3   | 0   | 0   | 0   | 32  | 0   | 0   | 3   | 0   | 0   | 0   | 2   | 0   |
| LI-RADS   | 100 | US       | 0   | 31  | 30  | 0   | 0   | 39  | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| NI-RADS   | 100 | CT       | 0   | 55  | 1   | 4   | 1   | 38  | 1   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| O-RADS    | 100 | MRI      | 1   | 1   | 39  | 0   | 0   | 22  | 12  | 0   | 0   | 0   | 25  | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| O-RADS    | 100 | US       | 2   | 3   | 49  | 0   | 0   | 25  | 5   | 0   | 0   | 0   | 16  | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| PI-RADS   | 100 | MRI      | 0   | 14  | 10  | 0   | 0   | 19  | 25  | 0   | 0   | 0   | 32  | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| TI-RADS   | 100 | US       | 0   | 3   | 9   | 0   | 0   | 17  | 23  | 0   | 0   | 0   | 33  | 0   | 0   | 0   | 15  | 0   | 0   | 0   | 0   |
| VI-RADS   | 100 | MRI, CT  | 0   | 9   | 28  | 0   | 0   | 14  | 21  | 0   | 0   | 0   | 21  | 0   | 0   | 0   | 7   | 0   | 0   | 0   | 0   |
| CAD-RADS  | 100 | CT       | 29  | 15  | 22  | 0   | 0   | 19  | 0   | 7   | 5   | 0   | 2   | 0   | 0   | 0   | 1   | 0   | 0   | 0   | 0   |
| LUNG-RADS | 100 | CT       | 0   | 34  | 27  | 0   | 0   | 9   | 4   | 10  | 16  | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |

<sup>E: equivocal; M: malignant; N: non-categorizable; NP: non-progressing; NV: non-viable; TIV: tumor-in-vein; V: viable</sup>

---

## Sample Reports

Below are representative samples from the RXL-RADSet dataset. Click on any report to view the full PDF.


### O-RADS Samples

| Report | Modality | Profile | RADS Score |
|--------|----------|---------|------------|
| [R013_O_MRI.pdf](assets/samples/O-RADS/MRI/R013_O_MRI.pdf) | MRI | 1 | 4 |
| [R076_O_US.pdf](assets/samples/O-RADS/US/R076_O_US.pdf) | Ultrasound | 1 | 2 |

### PI-RADS Samples

| Report | Modality | Profile | RADS Score |
|--------|----------|---------|------------|
| [R065_P_MRI.pdf](assets/samples/PI-RADS/R065_P_MRI.pdf) | MRI | 4 | 1 |

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

<!-- TODO: Uncomment to enable Citation section
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

---
-->



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
