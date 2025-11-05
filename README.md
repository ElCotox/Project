Step 1 — Preparation
  Run Section 1 — “Prep.”
  Cell 2 in this section creates the required folders
  
  All files needed are here in the repository download them, the xgb_model is too large to be uploaded on github so you can find it here : 
  https://www.dropbox.com/scl/fi/nsrthylfav3y02mn9wweg/xgb_model.json?rlkey=xlhitq6kgz6sownlufvy75j0l&st=d8rdvlz6&dl=0
  
  Place both PPF reports in:
  esg_rating_project/data/reports_to_analyze

  Place the rating module artifacts in:
    esg_rating_project/rating_module
      Files expected: feature_columns.json, sector_bias.csv, xgb_model.json.

Step 2 — Execution
Run all notebook cells in order (top to bottom), without skipping any.

Step 3 - Human in the loop

To speed things up, you can enter the KPI-selection data manually using the values from Tables 2 and 3 in the thesis (rating cell is replacing -1 by NaN)
For the KPI renewable_energy_pct, the extraction model looks for “% renewable,” but MSCI reports the non-renewable share --> NO problem for PPF its 50% either way :)

Performance note (Google Colab)
Due to VRAM limitations, we can’t load all models on the GPU.
As a result, preprocessing takes about 20 minutes, and retrieval and extraction take roughly the same amount of time.
