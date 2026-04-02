# Brain Tumor C-CNN pipeline

This repository implements a compact convolutional neural network (C-CNN) for multi class brain MRI tumour classification into four labels: **glioma**, **meningioma**, **pituitary tumour**, and **no tumour**.

The core contribution of this fork is a **reproducible training and evaluation pipeline** built via Google Colab (Pro) and the following notebook file is available in the pipeline folder:

- `BT_repro_pipeline_v2.ipynb`

## What this repository contains

- A compact CNN model intended for efficiency oriented experimentation.
- A training procedure using **augmentation during training only**, plus standard regularisation.
- Callback based optimisation, including early stopping and learning rate scheduling.
- A reporting workflow that separates model selection from final test evaluation.

## Reproducible pipeline notebook

Place the notebook `BT_paper_pipeline_v3_update_020426.ipynb` at the repository root. The notebook is expected to:

- control random seeds where supported
- keep training, validation, and test partitions distinct
- fit any data dependent transformations on training only
- report metrics on the untouched test subset once

Alternatively, you can run the .py file to reproduce it in your own server.
Please note that we strongly suggest to use at least some additional resources (L4, even better a T4) for high demanding GPU tasks through pipeline cells.


## Credits and provenance

We would like to express our sincere appreciation to the contributor of the repository:

https://github.com/sundussfatima/Tumor_classification_GUtech

The original project, indeed, provided the foundational implementation and experimental structure upon which this work builds. The present repository only refactors and reorganises that baseline for reproducibility.


If you reuse this work, please acknowledge both repositories.


## Installation

Create an isolated environment, then install dependencies:

```bash
pip install -r requirements.txt
```


## Notes on research use

This code is intended for research and educational use. It does not establish clinical utility, robustness to acquisition heterogeneity, or suitability for deployment in healthcare settings.

