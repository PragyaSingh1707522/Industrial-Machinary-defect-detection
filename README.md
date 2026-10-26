# Industrial Machinery Defect Detection

A deep learning-based project for detecting visual defects and anomalies in industrial machinery components using computer vision and anomaly detection techniques.

## Overview

Industrial quality inspection is essential for identifying manufacturing defects, surface irregularities, and abnormal patterns before products reach customers. Manual inspection can be time-consuming and inconsistent.

**Industrial Machinery Defect Detection** explores automated visual anomaly detection using the [Anomalib](https://github.com/open-edge-platform/anomalib) deep learning library. The framework provides implementations of anomaly detection algorithms that can be trained and evaluated on industrial image datasets.

The project can be adapted to identify defects such as scratches, cracks, dents, surface damage, and other visual abnormalities, depending on the dataset and trained model.

## Objectives

- Automate visual inspection of industrial components.
- Identify anomalous patterns in product images.
- Explore deep learning techniques for industrial quality control.
- Evaluate model performance on industrial inspection datasets.
- Support future integration into manufacturing inspection workflows.

## Technology Stack

- **Programming Language:** Python
- **Deep Learning:** PyTorch
- **Computer Vision:** Image-based anomaly detection
- **Anomaly Detection Framework:** Anomalib
- **Model Training:** PyTorch Lightning-based training workflows
- **Inference and Deployment:** Anomalib inference tools, with optional OpenVINO acceleration

## Project Structure

The repository follows the structure of the Anomalib framework. Key directories include:

```text
Industrial-Machinary-defect-detection/
├── src/
│   └── anomalib/       # Anomaly detection models and framework
├── examples/           # Example notebooks and workflows
├── tools/              # Training, inference, and utility tools
├── docs/               # Documentation
├── tests/              # Automated tests
├── application/        # Anomalib Studio application
├── pyproject.toml      # Project configuration and dependencies
├── uv.lock             # Dependency lock file, if included
├── LICENSE             # Original project license
└── README.md
```

The exact files and directories may vary with the version of Anomalib in the repository.

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/PragyaSingh1707522/Industrial-Machinary-defect-detection.git
cd Industrial-Machinary-defect-detection
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 3. Install Anomalib

For a standard installation:

```bash
python -m pip install --upgrade pip
pip install anomalib
```

For development using the source repository, follow the installation instructions and dependency requirements in the included `pyproject.toml` and the original [Anomalib documentation](https://anomalib.readthedocs.io/en/latest/).

**Note:** Hardware-specific PyTorch dependencies may need to be installed separately depending on whether you use a CPU, NVIDIA GPU, or supported Intel GPU.

## Model Training

Anomalib supports training anomaly detection models on supported datasets. For example, a PatchCore model can be trained using the MVTec AD dataset:

```bash
anomalib train --model Patchcore --data anomalib.data.MVTecAD
```

The dataset configuration, category, image paths, and model parameters should be adjusted for your specific industrial inspection use case.

## Inference

After training a model and obtaining a compatible checkpoint, use Anomalib's prediction workflow to evaluate new images.

```bash
anomalib predict \
  --model anomalib.models.Patchcore \
  --data anomalib.data.MVTecAD \
  --ckpt_path path/to/model.ckpt
```

Replace the example dataset and checkpoint path with the configuration appropriate for your trained model.

## Potential Applications

- Manufacturing quality inspection
- Surface defect detection
- Industrial component inspection
- Automated visual anomaly screening
- Production-line quality assurance

These are intended applications; actual detection performance depends on the dataset, training configuration, and evaluation results.

## Future Improvements

- Configure a dedicated industrial machinery dataset.
- Train and evaluate suitable anomaly detection models.
- Add quantitative evaluation metrics and sample predictions.
- Develop a simple interface for uploading inspection images.
- Explore real-time camera integration and optimized inference.
- Integrate the trained model into an industrial quality inspection pipeline.

## Original Project and Attribution

This project repository uses the open-source [Anomalib](https://github.com/open-edge-platform/anomalib) library as its underlying anomaly detection framework.

Anomalib provides deep learning algorithms, training and inference tools, and benchmarking capabilities for visual anomaly detection.

- **Original repository:** https://github.com/open-edge-platform/anomalib
- **Documentation:** https://anomalib.readthedocs.io/en/latest/
- **License:** Refer to the included `LICENSE` file and the original project's licensing terms.

All applicable copyright notices, license terms, and attribution requirements must be preserved.

## Disclaimer

This repository's title describes its intended application. A project-specific dataset, trained model, evaluation results, or custom interface should only be described as implemented after it has actually been developed and verified.

## Author and Contributions

Contributions that improve industrial defect detection workflows, dataset support, model evaluation, and deployment are welcome, subject to the applicable project license.
