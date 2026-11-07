# Method and reproducibility notes

## Research idea

The notebook explores a stochastic extension of TrivialAugment: sample the number of operations rather than fixing it to one. The current notebook implementation samples `num_ops` from 1 to 2 and samples operation magnitudes from the range defined in its augmentation class. Refer to the notebook itself for the exact code and any subsequent edits.

## Run

Execute `StochasticTrivialAugment.ipynb` from the first cell through the last. It contains the augmentation definitions, WideResNet, configuration, CIFAR-10 data pipeline, training loop, and observations.

## Dataset

CIFAR-10 is downloaded through torchvision into `./data` relative to the notebook kernel's working directory.

## Environment

Install dependencies from `requirements.txt`. The notebook uses PyTorch, torchvision, NumPy, and Pillow. A compatible CUDA/PyTorch installation is recommended for GPU training.

## Reproducibility checklist

For each run, record:
- Python, PyTorch, torchvision, NumPy, and Pillow versions
- GPU model and CUDA runtime
- random seed(s)
- number-of-operations sampling rule
- magnitude range and augmentation pool
- batch size, epochs, optimizer, learning-rate schedule, and data transforms
- evaluation protocol and reported metrics

## Interpretation

This is an exploratory research variant. Its results should be compared with the TrivialAugment baseline only when training and evaluation conditions are controlled. The notebook's recorded observations are not independently re-run as part of this documentation cleanup.
