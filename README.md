# us2024-election-toxicity

Data and analysis for the paper:

**"F*** You Biden": Cross-Partisan Electoral Toxicity on X**
Danishjeet Singh, Anindya Mondal, Filippo Menczer
Observatory on Social Media (OSoMe), Indiana University Bloomington

---

## Repository Contents

### Data (TODO: add files)
- `posts_preds.csv` — post IDs + GPT-4o-mini political leaning labels (Democrat / Republican / Unsure)
- `replies_preds.parquet` — reply IDs + per-reply political leaning labels + user ID + original post ID
- `posts_tox_scores.csv` — post IDs + Perspective API toxicity scores
- `replies_tox_scores.csv` — reply IDs + Perspective API toxicity scores

> Raw tweet text is not released in accordance with X's Terms of Service. Use the tweet IDs to rehydrate via the X API.

### Prompts (TODO: add file)
- `prompts.md` — full system and user prompts used for GPT-4o-mini post and reply classification (also reproduced in paper Appendix)

### Analysis (TODO: add notebook)
- `final_analysis.ipynb` — reproduces all reported results: MWU tests, figures, composition statistics

---

## Dataset

Built on top of the [US2024-Twitter-Elections](https://github.com/osome-iu/US2024-Twitter-Elections) dataset.
Covers May–November 2024. \~261k original posts and \~2.4M direct replies.

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
