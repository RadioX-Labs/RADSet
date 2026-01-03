# RXL-RADSet

![RXL-RADSet](https://img.shields.io/badge/Dataset-RXL--RADSet-blue)
![License](https://img.shields.io/badge/License-CC--BY--NC--SA%204.0-lightgrey)

**RXL-RADSet: A Radiologist-Validated Synthetic Benchmark for Language Models**

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
| NI-RADS   | 200 | 0   | 0           | 0          | 200   |
| O-RADS    | 0   | 100 | 0           | 100        | 200   |
| PI-RADS   | 0   | 100 | 0           | 0          | 100   |
| TI-RADS   | 0   | 0   | 0           | 100        | 100   |
| VI-RADS   | 0   | 100 | 0           | 0          | 100   |

### RADS Score Distribution

| **RAD**         | **N**  | **0** | **1** | **2** | **2a** | **2b** | **3**  | **4** | **4A** | **4B** | **4C** | **5**  | **6** | **Equivocal** | **M** | **N** | **NC** | **TIV** | **V** |
| --------------- | ----- | ----- | ----- | ----- | ------ | ------ | ------ | ----- | ------ | ------ | ------ | ------ | ----- | ------------- | ----- | ----- | ------ | ------- | ---- |
| BI-RADS         | 300   | 9     | 31    | 75    |        |        | 50     | 33    | 15     | 23     | 8      | 31     | 25    |               |       |       |        |         |      |
| CAD-RADS        | 100   | 29    | 15    | 22    |        |        | 19     |       | 7      | 5      |        | 2      |       |               | 1     |       |        |         |      |
| GB-RADS         | 100   | 8     | 29    | 33    |        |        | 14     | 6     |        |        |        | 10     |       |               |       |       |        |         |      |
| LI-RADS         | 400   |       | 73    | 40    |        |        | 106    | 6     |        |        |        | 68     |       | 5             |       |       |        | 2       |      |
| LR-TR           | 100   |       |       |       |        |        |        |       | 2      |        | 1      | 14     | 63    |               | 20    |       |        |         |      |
| NI-RADS (Primary)| 100  |       | 55    | 1     | 4      | 1      | 38     | 1     |        |        |        |        |       |               |       |       |        |         |      |
| NI-RADS (Nodal) | 100   |       | 66    | 11    |        |        | 23     |       |        |        |        |        |       |               |       |       |        |         |      |
| O-RADS          | 200   | 3     | 4     | 88    |        |        | 47     | 17    |        |        |        | 41     |       |               |       |       |        |         |      |
| PI-RADS         | 100   |       | 14    | 10    |        |        | 19     | 25    |        |        |        | 32     |       |               |       |       |        |         |      |
| TI-RADS         | 100   |       | 3     | 12    |        |        | 15     | 22    |        |        |        | 33     |       |               |       | 15    |        |         |      |
| Lung-RADS       | 100   |       | 34    | 27    |        |        | 9      | 4     | 10     | 16     |        |        |       |               |       |       |        |         |      |
| VI-RADS         | 100   |       | 9     | 28    |        |        | 14     | 21    |        |        |        | 21     |       |               |       | 7     |        |         |      |

<sup>NI-RADS includes both Primary (100) and Nodal (100) categories. LI-RADS includes LR-TR (100) as a separate category.</sup>

---

## Dataset Creation

### Synthetic Generation

RXL-RADSet is a comprehensive, multi-domain dataset of radiology reports based on major Reporting and Data Systems (RADS), including BI-RADS, PI-RADS, O-RADS, LI-RADS, NI-RADS, and others. All reports were **synthetically generated** using large language models (LLMs) including GPT (OpenAI), Claude (Anthropic), and Gemini (Google) according to explicit, domain-tailored scenario plans.

**No real patient data were used**; all content was fictitious, created de novo for academic and benchmarking purposes.

### Scenario Planning

For each RADS domain, rigorous scenario design was established to reflect realistic clinical diversity. This included stratification by:

- Imaging modality
- Anatomy
- Risk class
- Lesion type
- Staging features
- Specific reporting system

For every RADS, a broad mix of clinical situations was modelled to ensure representative coverage, including low-, intermediate-, and high-risk scenarios across typical lesion topographies. Prompting strategies for LLMs were carefully constructed, with reports generated sequentially for each scenario to ensure both stylistic and clinical heterogeneity.

### Radiologist Profiles

To enhance clinical realism and heterogeneity, synthetic reports were generated according to a spectrum of **five simulated radiologist profiles**:

| Profile | Experience | Description |
|---------|------------|-------------|
| **Profile 1** | <5 years, general radiology | Junior attendings using templated language, thorough but concise, with cautious wording (e.g., "may represent", "suspicious for") and moderate analytic depth |
| **Profile 2** | 5–10 years, general radiology | Mid-career generalists comfortable with the target modality, displaying pattern recognition, semi-structured reports, balanced confidence, and moderate narrative flow |
| **Profile 3** | <5 years, subspecialty | Recent fellowship-trained or early-career subspecialists (e.g., breast, GU, liver) with highly structured, systematic, detail-rich style, precise lesion localization and scoring, and academic language |
| **Profile 4** | >5 years, subspecialist | High-volume practice; concise, confident reports focusing on staging and major findings, omitting minor details, and employing mature clinical language |
| **Profile 5** | Resident | Overly detailed, occasionally verbose reports with explicit mention of all findings, frequent reiteration, and slightly tentative interpretation in borderline cases |

Each profile was mapped to distinct scenario templates for each RADS system, promoting diversity in both report style and content.

### Quality Assurance

All LLM-generated reports underwent **expert review in two layers**:

1. **First-layer screening**: Every report was assessed by a senior radiologist with over 13 years of post-training experience for overall correctness, completeness, and adherence to clinical reality. Reports failing this screen were either removed or flagged for revision.

2. **Second-layer domain review**: All reports passing first-layer review were subsequently evaluated and, if necessary, corrected by subspecialty radiologists expert in the specific RADS domain (e.g., breast, prostate, liver, gynecologic, head and neck). This ensured technical accuracy and authentic style of each system's reporting conventions.

### Metadata

Each report in the dataset is accompanied by standardized metadata, including:
- RADS system
- Imaging modality
- Assigned RADS score
- Radiologist profile used for generation

All synthetic reports were anonymized and de-identified at creation and remain free of any protected health information (PHI).

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
  author={First Author and Second Author},
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

For questions about the dataset, access requests, or collaboration opportunities, please contact:
- **Email:** dummy.email@example.com

---

<!-- TODO: Uncomment and add acknowledgments
## Acknowledgments
-->
