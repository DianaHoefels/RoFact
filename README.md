
# RoFact: A Romanian Fact-Checking Dataset

## License

[![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)

The dataset is released under **Creative Commons Attribution 4.0 International (CC BY 4.0)**, with express permission from factual.ro.
Please attribute both the dataset author (Diana Höfels) and the original source (Factual.ro by Funky Citizens) in any academic use or derived work.

You are free to use, share, and adapt the data, as long as you give proper credit.

**Author**: Diana Höfels  
**Version**: 1.0  
**Date**: 2025-06-21  
**:octocat: GitHub Repository**: [https://github.com/dianahoefels/rofact](https://github.com/dianahoefels/rofact)

**🤗Hugging Face Repository**:  [Hugging Face Hub](https://huggingface.co/datasets/dianahoefels/rofact)

---

## Overview

**RoFact** is a manually compiled dataset of Romanian political and public-domain claims labeled with expert fact-checking verdicts.  
It was collected from [factual.ro](https://www.factual.ro), the leading Romanian fact-checking platform run by Funky Citizens.  
The current version (v1.0) includes **789 expert-annotated claims**, covering domains such as economy, healthcare, education, and governance.

The dataset is split into:
- **Training set**: 552 samples (70%)
- **Validation set**: 118 samples (15%)
- **Test set**: 119 samples (15%)

🛑 **Note**: The test set is not publicly released.

🔐 **Access to Test Set**

To support fair benchmarking and potential use in shared tasks, challenges, or hackathons, the **test split of RoFact is not publicly released**.

Researchers, educators, and developers who wish to access the test set for academic or evaluation purposes are kindly invited to reach out via email. 

Access may be granted upon request for non-commercial, research-aligned use.


📩 If you are a researcher or developer interested in accessing the test set for academic or benchmarking purposes, please contact:

**Diana Höfels**  
📬 Email: diana.hoefels@gmail.com

All claims were collected from [factual.ro](https://www.factual.ro), the Romanian fact-checking platform operated by Funky Citizens, and are used with permission for academic and research purposes.
The dataset includes metadata such as speaker, verdict, topic, and source link.  
The current version of RoFact (v1.0) includes all claims published on factual.ro up to **November 28, 2024**.

---

## Dataset Structure

| Column         | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `claim_id`     | Unique ID or URL slug                                                       |
| `claim_text`   | The main text of the claim (short statement made by a public figure)        |
| `speaker`      | Person who made the claim                                                   |
| `date`         | Original publication date (YYYY-MM-DD)                                      |
| `verdict`      | Fact-checking label (`Adevărat`, `Fals`, `Parțial Adevărat`, `Trunchiat`)   |
| `topic`        | Topic category (e.g., economy, health, education)                           |
| `source_url`   | Link to the original fact-checking article                                  |

### Verdict Labels

The `verdict` column includes the following expert-assigned categories:

- **Adevărat** `True`
- **Fals** `False`
- **Imposibil de verificat**`Impossible to verify`
- **Numai cu sprijin instituțional** `Only with institutional support`
- **Parțial adevărat** `Partially true`
- **Parțial fals** `Partially false`
- **Trunchiat** `Truncated`

[See `data/stats.md` for label distribution and frequency breakdown.](./data/stats.md)

All entries have been cleaned and formatted for ease of use in machine learning pipelines.

---

## Example
---

```tsv
claim_id	claim_text	speaker	date	verdict	topic	source_url
1001	„România a avut cea mai mare creștere economică din UE în 2023.”	Marcel Ciolacu	2023-12-12	Adevărat	Economie	https://www.factual.ro/...
```
---

### 🔐 Access to Test Set

To ensure fair evaluation and potential use in future shared tasks or hackathons, the **test split is not publicly released**.

📩 If you are a researcher or developer interested in accessing the test set for academic or benchmarking purposes, please contact:

**Diana Höfels**  
📬 Email: diana.hoefels@gmail.com

---
## Reproduction & Scripts

To reproduce or regenerate the dataset, run:

```bash
python scripts/scrape_factual.py --output data/rofact_20241128.tsv
```
Other utility scripts are provided for preprocessing and filtering.

---

## Source

factual.ro (Funky Citizens).

Dataset compiled and formatted by Diana Höfels (2024).

---

## Permissions:

Use of factual.ro content in this dataset has been authorized by the platform’s editorial team for the purposes of academic research and reproducibility.
The dataset may not be used for commercial purposes or republished elsewhere without contacting both the dataset author and factual.ro.

## Acknowledgements

Thanks to factual.ro and Funky Citizens for their open data approach and ongoing commitment to transparency in Romanian public discourse.

---

## Contact

For questions, suggestions, or collaborations:

📬 Email: your.email@uni-tuebingen.de

:octocat: GitHub: [@dianahoefels](https://github.com/dianahoefels)


---
## Citation

```bibtex
@misc{hoefels2024rofact,
  title={{RoFact}: A Romanian Fact-Checking Dataset},
  author={Diana H{\"o}fels},
  year={2024},
  howpublished={\url{https://github.com/dianahoefels/rofact}}
}
