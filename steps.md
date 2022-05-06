- cml basics

  - cml uses to write into a report.md

- dvc
  - dvc init # init project
  - define file
  ```
  stages:
      train:
          cmd: python train.py
          deps:
          - train.py
          - wine_quality.csv
          outs:
          - metrics.txt
          - feature_importance.png
          - residuals.png
          metrics:
          - metrics.json:
              cache: false # so don't rely on local caches
  ```
  - dvc repro
