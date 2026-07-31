# 🧾 OpenReview-200 Review Dataset

## 📘 Overview

This repository contains the **OpenReview-200** dataset, a curated collection of authentic and AI-generated scientific peer reviews developed as part of a funded research project under the supervision of **Dr. Junaid Shuja**, Tenure Track Assistant Professor, Department of Computer Science, Southeast Missouri State University, USA.

The dataset supports research on understanding the differences between human-written and AI-generated peer reviews and facilitates studies in AI-generated scientific text detection, peer review quality assessment, and trustworthy AI.



## 📊 Dataset Description

The dataset was curated from the publicly available **ICLR OpenReview** corpus (ICLR 2017), originally released by Wang et al. (2023).

To construct the dataset:

- **200 Authentic Reviews** were selected from 200 unique ICLR 2017 papers.
- **200 AI-Generated Reviews** were created for the same papers using **DeepSeek**, based on each paper's title and abstract.

The resulting dataset contains **400 reviews** corresponding to **200 unique papers**, where each paper has one authentic review and one AI-generated review, enabling direct one-to-one comparison.



## 🗂️ Data Format

The dataset is provided in CSV format with the following columns:

| Column Name | Description |
|-------------|-------------|
| Article Title | Title of the research paper |
| Abstract | Abstract of the paper |
| Review | Full peer review text |
| Review Type | Indicates whether the review is Authentic or AI-Generated |

### Review Type Values

- Authentic
- AI-Generated



## 🔄 Pairing Strategy

Each authentic review is paired with its corresponding AI-generated review using a normalized article title. Titles were converted to lowercase, extra spaces were removed, and any scraped **"OpenReview"** suffix was stripped to ensure correct one-to-one matching.



## 🧩 Funding and Supervision

This dataset was developed as part of a **Graduate Research Funding Committee (GRFC)** funded research project at **Southeast Missouri State University (SEMO)** under the supervision of **Dr. Junaid Shuja**.



## 📚 Data Source

The authentic reviews originate from the publicly available **ICLR OpenReview** dataset:

> Wang et al. (2023). *Have LLMs Reached the Human Level in Open-Domain Dialogue?* (ICLR OpenReview corpus)

Repository:
https://github.com/Seafoodair/Openreview



## ⚠️ Note

This dataset supports ongoing research and may be updated following peer review or publication.

If you use this dataset in your research, please cite this repository.



## 📄 Citation

A formal citation will be added after the associated research paper is published.
