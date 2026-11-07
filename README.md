# Stochastic TrivialAugment

A research experiment that modifies TrivialAugment by sampling the number of augmentation operations per image rather than always applying exactly one operation. The notebook describes the proposed variant and evaluates it with a CIFAR-10 / WideResNet training pipeline.

## Quick start

Open `StochasticTrivialAugment.ipynb` in Jupyter or Google Colab and run the cells sequentially.

```bash
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows PowerShell: .venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
jupyter notebook StochasticTrivialAugment.ipynb
```

A CUDA-capable GPU is recommended.

## Layout

- `StochasticTrivialAugment.ipynb` — canonical implementation and experiment.
- `docs/REPRODUCIBILITY.md` — method, environment, and run notes.
- `requirements.txt` — Python dependencies.

## Method at a glance

The notebook samples a number of operations (currently from one or two), samples operations from the augmentation pool, and scales the sampled magnitude range relative to the number of operations. The exact implementation and configuration in the notebook are authoritative.

## Data and results

The experiment uses CIFAR-10 downloaded by torchvision into `./data`. The notebook contains its reported training observations. Treat these as results from the recorded experiment, not as an independently verified claim.

The original notebook is preserved unchanged in this cleanup branch.
