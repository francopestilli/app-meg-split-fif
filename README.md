# Split MEG files

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Splits a raw MEG recording into two FIF files covering two user-defined time windows, using MNE-Python.**

Reads the raw MEG file with MNE-Python and saves the segment from t1min to t1max as the first output and the segment from t2min to t2max as the second. Use it to separate, for example, two runs or conditions recorded in one file. Times are in seconds and must lie within the recording.

| | |
|---|---|
| 📥 **Inputs** | `neuro/meeg/mne/raw` |
| 📤 **Outputs** | `neuro/meg/fif` ×2 |
| 🐳 **Container** | `brainlife/mne:0.23dev` |
| ⚙️ **Resources** | 8 CPUs · 0.17 h walltime |
| 🔗 **Run it** | [doi.org/10.25663/brainlife.app.529](https://doi.org/10.25663/brainlife.app.529) |

#### 📥 Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `raw01` | `neuro/meeg/mne/raw` | yes | Raw MEG recording readable by mne.io.read_raw (e.g. FIF). |

#### 📤 Outputs

| Output | Datatype | Description |
|---|---|---|
| `out_dir1` | `neuro/meg/fif` | FIF file with the first time window (t1min to t1max). |
| `out_dir2` | `neuro/meg/fif` | FIF file with the second time window (t2min to t2max). |

<details>
<summary><b>⚙️ Parameters</b> (4)</summary>

| Parameter | Type | Default | Description |
|---|---|---|---|
| `t1min` | number | `0` | Start of the first segment, in seconds. |
| `t1max` | string | `100` | End of the first segment, in seconds. |
| `t2min` | number | `100` | Start of the second segment, in seconds. |
| `t2max` | number | `200` | End of the second segment, in seconds. |

</details>

📚 **References used by this App:**
- Gramfort A, et al. MEG and EEG data analysis with MNE-Python. Front Neurosci 7:267 (2013). [doi:10.3389/fnins.2013.00267](https://doi.org/10.3389/fnins.2013.00267)

<!-- brainlife-app:end -->

[![Abcdspec-compliant](https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg)](https://github.com/brain-life/abcd-spec)
[![Run on Brainlife.io](https://img.shields.io/badge/Brainlife-bl.app.529-blue.svg)](https://doi.org/10.25663/brainlife.app.529)


## Documentation
This Brainlife App splits MEG files 


## Authors
- [Guiomar Niso](guiomar.niso@ctb.upm.es), Instituto Cajal, CSIC, Spain

## Citations
We kindly ask that you cite the following articles when publishing papers and code using this app. 

1. **brainlife. io: A decentralized and open source cloud platform to support neuroscience research**. Hayashi, S., Caron, B. A., et al. & Pestilli, F. (2023). ArXiv. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10274934/

2. **MEG and EEG data analysis with MNE-Python**. Gramfort A, et al. & Hämäläinen MS. (2013). Frontiers in Neuroscience, 7(267):1–13, 2013. https://doi.org/10.3389/fnins.2013.00267

## Funding Acknowledgement
brainlife.io is publicly funded and for the sustainability of the project we kindly ask that you acknowledge the following funding sources:

[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-1636893](https://img.shields.io/badge/NSF_BCS-1636893-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-ACI-1916518](https://img.shields.io/badge/NSF_ACI-1916518-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1916518)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NIH-NIBIB-R01EB030896](https://img.shields.io/badge/NIH_NIBIB-R01EB030896-green.svg)](https://grantome.com/grant/NIH/R01-EB030896-01)


#### MIT Copyright (c) 2021 brainlife.io The University of Texas at Austin and Indiana University