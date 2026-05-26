# Crouzon-PUACT: Dataset of Paired Preoperative and Postoperative Upper Respiratory Tract CT Images for in Patients with the Crouzon Syndrome

**Crouzon-PUACT** is a paired preoperative and postoperative craniofacial CT dataset for upper airway analysis in patients with Crouzon syndrome.

The dataset contains paired CT volumes and corresponding upper airway segmentation masks. It is intended to support automated upper airway segmentation, longitudinal airway morphology analysis, and surgical outcome assessment in craniofacial deformity research.

Due to the sensitive nature of human craniofacial CT images from a rare disease cohort, including paediatric patients, the CT images and segmentation masks are provided under **controlled access** through Science Data Bank.

---

## Overview

Crouzon syndrome is a rare craniosynostosis syndrome characterized by complex craniofacial skeletal abnormalities. Upper airway morphology is clinically relevant in this population, particularly before and after midface advancement surgery.

Crouzon-PUACT provides paired preoperative and postoperative CT imaging data with manually annotated upper airway segmentation masks. The paired design enables longitudinal comparison of airway morphology before and after surgery.

The restricted CT images and segmentation masks are **not stored in this GitHub repository**.

---

## Dataset Access

The dataset is deposited in **Science Data Bank (ScienceDB)** under controlled access.

- Dataset name: `Crouzon-PUACT`
- Dataset DOI / accession number: `To be inserted`
- ScienceDB URL: `To be inserted`

Researchers who wish to access the restricted CT images and segmentation masks should submit a data access request through the ScienceDB dataset page and agree to the Data Usage Agreement.

Access applicants will be asked to provide verifiable identity and affiliation information and to confirm that they will not:

- attempt to re-identify participants;
- redistribute the data to unauthorized users;
- use the data outside the permitted research purposes;
- publish or release data derivatives that may compromise participant privacy.

---

## Why Controlled Access?

Although all files have been de-identified, this dataset contains three-dimensional craniofacial CT images from patients with a rare disease, including paediatric patients. Craniofacial CT volumes may retain individual anatomical features and therefore may carry a potential risk of participant re-identification.

For this reason, the dataset is shared under controlled access rather than unrestricted open download. The controlled access model is intended to balance scientific reuse with participant privacy protection.

---

## Dataset Organization

After access is granted, the released dataset is organized as follows:

```text
images/
├── L001_pre_img.nrrd
├── L001_pos_img.nrrd
├── L002_pre_img.nrrd
├── L002_pos_img.nrrd
└── ...
labels/
├── L001_pre_seg.nrrd
├── L001_pos_seg.nrrd
├── L002_pre_seg.nrrd
├── L002_pos_seg.nrrd
└── ...

Filenames follow a standardized convention consisting of:
anonymous subject identifier + surgical stage + data type
where:
L001 is the anonymous subject identifier;
pre indicates the preoperative CT;
pos indicates the postoperative CT;
img indicates the CT image volume;
seg indicates the segmentation mask.
```
Thus, L001_pre_img.nrrd and L001_pre_seg.nrrd represent the preoperative CT image and corresponding segmentation mask of subject L001, respectively. L001_pos_img.nrrd and L001_pos_seg.nrrd represent the corresponding postoperative CT image and segmentation mask.

---
## Label Definitions
The segmentation masks use integer labels.

The current label definition is:
```text
0 = background
1 = right nasal cavity
2 = left nasal cavity
3 = nasopharynx
```

![image](https://github.com/fuguer733/Crouzon-PUACT/blob/main/example.png)
## nnU-Net Baseline

The baseline segmentation experiments are based on [nnUNet](https://github.com/MIC-DKFZ/nnUNet).

This repository does not redistribute the nnU-Net source code. Please install nnU-Net from the official repository




