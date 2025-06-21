
# RoFact: A Romanian Fact-Checking Dataset

## License

[![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)
[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Released under **Creative Commons Attribution 4.0 International (CC BY 4.0)**.  

You are free to use, share, and adapt the data, as long as you give proper credit.

**Author**: Diana Höfels  
**Version**: 1.0  
**Date**: 2025-06-21  
**:octocat: GitHub Repository**: [https://github.com/dianahoefels/rofact](https://github.com/dianahoefels/rofact)

---

## Overview

**RoFact** is a manually compiled dataset of Romanian political and public-domain claims labeled with expert fact-checking verdicts.  
It is designed for research in **claim verification**, **fake news detection**, and **cross-lingual transfer learning**, especially for **low-resource languages**.

All claims were collected from [factual.ro](https://www.factual.ro), a trusted Romanian fact-checking platform run by Funky Citizens.  
The dataset includes metadata such as speaker, verdict, topic, and source link.  
The current version of RoFact (v1.0) includes all claims published on factual.ro up to **November 28, 2024**.

Also available on 🤗 Hugging Face::  [Hugging Face Hub](https://huggingface.co/datasets/dianahoefels/rofact)

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
