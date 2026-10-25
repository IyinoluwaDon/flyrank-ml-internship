# FlyRank Applied Search Intelligence and ML Internship

An applied machine-learning curriculum and reproducible search-ranking workflow built around an anonymized slice of real FlyRank search data. The project moves from a business question and data contract through feature construction, transparent baselines, model training, evaluation, and an action-oriented review queue.

## Data and models

The bundled `data/raw/content_refresh_anonymized.csv` contains roughly 30,000 anonymized page records. The larger gated FlyRank warehouse release is documented in the course materials. The runnable pipeline compares a transparent rule-based score with logistic regression, a decision tree, and a random forest using a client-holdout split. The sample workflow reports Precision@50 of roughly 0.24 for the hand-built baseline and 0.68-0.74 for the learned model, depending on library versions.

## Run the pipeline

```sh
pip install -r requirements.txt
python scripts/run_all.py
```

The pipeline writes a model report, review queue, and charts to `outputs/`. `notebooks/` contains the first-look and modeling lessons; `work/notebooks/` contains assignment and capstone notebooks; `docs/` contains the data dictionary, methodology, and setup guides. The repository's course instructions explain how learners create and submit their own copy.
