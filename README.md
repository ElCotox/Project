Step 1 — Preparation

Run Section 1 — “Prep.”

Cell 2 in this section creates the required folders:

Place both PPF reports in:
esg_rating_project/data/reports_to_analyze

Place the rating module artifacts in:
  esg_rating_project/rating_module
    Files expected: feature_columns.json, sector_bias.csv, xgb_model.json.

Step 2 — Execution

Run all notebook cells in order (top to bottom), without skipping any.

Performance note (Google Colab)

Due to VRAM limitations, we can’t load all models on the GPU.
As a result, preprocessing takes about 20 minutes, and retrieval and extraction take roughly the same amount of time.
