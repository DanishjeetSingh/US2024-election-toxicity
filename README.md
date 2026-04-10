# "F&#42;&#42;&#42; You Biden": Cross-Partisan Electoral Toxicity on X

Data and code for the paper accepted at the **7th International Workshop on Cyber Social Threats (CySoc 2026)** at ICWSM 2026.

**Authors:** Danishjeet Singh, Anindya Mondal, Filippo Menczer
Observatory on Social Media (OSoMe), Indiana University Bloomington

---

## Repository Contents

### Data (`data/`)

- `all_posts_data.parquet` — 261,501 original posts with tweet ID, GPT-4o-mini political leaning label (Democrat / Republican / Unsure), and Perspective API toxicity score.
- `all_replies_data.parquet` — 2,415,781 direct replies with reply ID, per-reply political leaning label, user ID, original post ID, and toxicity score.
- `gold_standard_posts_384.parquet` — 384-item human-annotated gold standard for the post classifier. Contains tweet ID, human consensus label (`final_label`), and GPT-4o-mini prediction (`political_leaning_pred`).
- `gold_standard_replies_384.parquet` — 384-item human-annotated gold standard for the reply classifier. Same structure as above.
- `prompt_posts.txt` — System and user prompts used to classify the political leaning of original posts.
- `prompt_replies.txt` — User prompt used to classify the political leaning of reply authors, given the original tweet, reply text, and author bio.

### Code

- `analysis.ipynb` — Reproduces all reported results: MWU tests with effect sizes (Cliff's delta), KDE figures, partisan composition statistics, unique user counts, and classifier F1 scores on the gold standard.

---

## Dataset

Uses data from the [x-24-us-election](https://github.com/sinking8/x-24-us-election) dataset, covering May–November 2024.

## Models Used
- **Political classification:** `gpt-4o-mini-2024-07-18` via OpenAI API
- **Toxicity scoring:** Perspective API

## Citation

```bibtex
@inproceedings{singh2026crosspartisan,
  title={"F*** You Biden": Cross-Partisan Electoral Toxicity on X},
  author={Singh, Danishjeet and Mondal, Anindya and Menczer, Filippo},
  booktitle={Proceedings of the ICWSM Workshop},
  year={2026}
}
```
