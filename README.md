# 🧾 OpenReview-200 Review Datasets (Persona and Neutral)

## 📘 Overview

This repository contains two versions of the **OpenReview-200** dataset, curated collections of authentic and AI-generated scientific peer reviews developed as part of a funded research project under the supervision of **Dr. Junaid Shuja**, Tenure Track Assistant Professor, Department of Computer Science, Southeast Missouri State University, USA.

- **OpenReview-200-Persona**: the original dataset. AI reviews were generated with a persona prompt.
- **OpenReview-200-Neutral**: AI reviews were regenerated with a neutral prompt and a 200–250-word limit.

Both datasets cover the **same 200 papers** and share the **same 200 authentic reviews**. Only the AI-generated reviews differ.

The datasets support research on the differences between human-written and AI-generated peer reviews, and on AI-generated scientific text detection, peer review quality assessment, and trustworthy AI. Because the papers and human reviews are identical, the two datasets also let researchers measure how the generation prompt affects AI reviews.



## 📁 Repository Contents

| File | Dataset | AI review prompt |
|------|---------|------------------|
| `openreview200_persona.csv` | OpenReview-200-Persona | Persona prompt, no length limit |
| `openreview200_neutral.csv` | OpenReview-200-Neutral | Neutral prompt, 200–250 words |



## 🆚 Comparison of the Two Datasets

| | OpenReview-200-Persona | OpenReview-200-Neutral |
|---|---|---|
| Papers | 200 ICLR 2017 papers | Same 200 papers |
| Authentic reviews | 200 | Same 200 reviews |
| AI-generated reviews | 200 | 200 |
| Generation model | DeepSeek | DeepSeek |
| Prompt style | Informal, first-person style of an ICLR 2017 reviewer | Standard peer review, no persona or style instruction |
| Length constraint | None | 200–250 words |
| Total reviews | 400 | 400 |

The persona prompt could leave a style of its own in the AI reviews. The neutral dataset removes that factor, so differences between human and AI reviews there are not caused by a persona instruction. We recommend **OpenReview-200-Neutral** as the main dataset for human-vs-AI comparisons. OpenReview-200-Persona is kept for transparency and for studying prompt effects.



## 📊 Dataset Construction

Both datasets were curated from the publicly available **ICLR OpenReview** corpus (ICLR 2017 file, `tp_2017conference.xlsx`), originally released by Wang et al. (2023).

1. **Authentic reviews:** 200 unique ICLR 2017 papers were selected, keeping one authentic reviewer report per paper. These 200 reviews appear in both datasets.
2. **AI-generated reviews:** for each paper, one AI review was generated with **DeepSeek**, once with the persona prompt and once with the neutral prompt.

Each dataset contains **400 reviews** for **200 unique papers**. Each paper has one authentic review and one AI-generated review, which allows direct one-to-one comparison.



## 💬 Generation Prompts

### Persona prompt (OpenReview-200-Persona)

The persona prompt asks the model to write in the informal, first-person style of an ICLR 2017 reviewer.

### Neutral prompt (OpenReview-200-Neutral)

> You are a peer reviewer with expertise in machine learning. Read the submitted paper and review it. Your review must be between 200 and 250 words long.

The neutral prompt contains no venue, year, persona, tone, or style instruction. The word limit keeps the AI reviews close to the typical length of the human reviews and reduces length as a confounding factor.

**Length compliance of the neutral AI reviews:**

| Statistic | Value |
|---|---|
| Mean length | 230 words |
| Standard deviation | 14.8 words |
| Range | 195–265 words |
| Within the requested 200–250 words | 91% |



## 🗂️ Data Format

Both CSV files use the same columns:

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

Within each dataset, each authentic review is paired with its corresponding AI-generated review using a normalized article title. Titles were converted to lowercase, extra spaces were removed, and any scraped **"| OpenReview"** suffix was stripped to ensure correct one-to-one matching.

The same normalized titles can be used to join the two datasets and compare the persona and neutral AI reviews for the same paper.



## 🧩 Funding and Supervision

These datasets were developed as part of a **Graduate Research Funding Committee (GRFC)** funded research project at **Southeast Missouri State University (SEMO)** under the supervision of **Dr. Junaid Shuja**.



## 📚 Data Source

The authentic reviews originate from the publicly available **ICLR OpenReview** dataset:

> Wang et al. (2023). *Have LLMs Reached the Human Level in Open-Domain Dialogue?* (ICLR OpenReview corpus)

Repository: https://github.com/Seafoodair/Openreview



## ⚠️ Note

These datasets support ongoing research and may be updated following peer review or publication.

If you use either dataset in your research, please cite this repository.



## 📄 Citation

A formal citation will be added after the associated research paper is published.
