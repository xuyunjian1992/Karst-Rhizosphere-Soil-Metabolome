# Raw LC–MS metabolomics data: rhizosphere soils of dominant grasses in a karst rocky desertification ecosystem

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Overview

This repository hosts the raw untargeted metabolomics data (mzXML format, positive and negative ESI modes) supporting the manuscript:

> **A rhizosphere bacterial–AMF consortium improves phosphorus nutrition and growth of a native grass under extreme phosphorus limitation in karst rocky desertification**
> Yunjian Xu, Weihao Cai, Zhe Chen\*, Xingwu Duan\*
> (*corresponding authors: zhechen2019@ynu.edu.cn; xwduan@ynu.edu.cn)

Soil samples were collected in September 2023 at the Karst Rocky Desertification Field Observation Station, Kaiyuan City, Yunnan Province, Southwest China (23°30′–23°59′N, 103°34′–103°43′E), from the rhizospheres of three dominant grasses — *Themeda japonica*, *Eulalia quadrinervis*, and *Heteropogon contortus* — and from unplanted bulk soil (control).

## File naming convention

```
{SampleID}_{MODE}.mzXML
```

- `SampleID`: group letter (A / B / C / D / K) + biological replicate number (1–5)
- `MODE`: `POS` (positive ESI mode) or `NEG` (negative ESI mode)
- `QC01–QC04`: quality-control samples (pooled aliquots of all samples), injected at regular intervals to monitor instrument stability

**Group mapping** *(please confirm before making the repository public)*:

| Prefix | Group | n |
|--------|-------|---|
| A1–A5 | *[group name, e.g., bulk soil]* | 5 |
| B1–B5 | *[group name]* | 5 |
| C1–C5 | *[group name]* | 5 |
| D1–D5 | *[group name]* | 5 |
| K1–K5 | *[group name]* | 5 |
| QC01–QC04 | Pooled quality control | 4 |

Total: 25 samples × 2 ion modes + 4 QC × 2 modes = **58 mzXML files** (~290 MB).

## Data acquisition

- **Chromatography**: Vanquish UHPLC system (Thermo Fisher Scientific), Phenomenex Kinetex C18 column
- **Mass spectrometry**: Orbitrap Exploris 120 (Thermo Fisher Scientific), electrospray ionization (ESI), positive and negative modes acquired separately
- **Acquisition software**: Xcalibur 3.1
- **Format conversion**: vendor `.raw` → `.mzXML` with ProteoWizard (msConvert, v3.0.22335), peak picking enabled
- **Note**: the deposited mzXML files contain MS1 full-scan spectra

## Data processing (summary)

Raw data were processed with XCMS in R for peak detection, retention-time correction, and alignment. Metabolic features were annotated against the HMDB and KEGG databases. Differential metabolites were screened with OPLS-DA (VIP > 1, fold change ≥ 2, *P* < 0.05). Full methodological details are provided in the manuscript (Section 2.6).

## Related resources

- **Amplicon sequencing data** (16S rRNA / ITS / AMF 18S): NCBI BioProject *[accession to be added]*
- **Analysis code and additional data**: see the main repository for this study

## License

These data are released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). If you use the data, please cite the associated manuscript.

## Contact

- Zhe Chen — zhechen2019@ynu.edu.cn
- Xingwu Duan — xwduan@ynu.edu.cn

State Key Laboratory of Vegetation Structure, Function and Construction (VegLab), School of Ecology and Environmental Sciences, Yunnan University, Kunming 650091, PR China
