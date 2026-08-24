# Q-RMC

![PyTorch](https://img.shields.io/badge/PyTorch-2.2.2-EE4C2C?logo=pytorch)
![Python](https://img.shields.io/badge/Python-3.10-3776AB?logo=python)

## Dataset

Prepare the synchronized and segmented multimodal data yourself.

```text
Q-RMC/data/
├── qrmc_dataset.npz
├── pu_qrmc.npz
├── seu_qrmc.npz
└── cwru_qrmc.npz
```

Install the environment:

```bash
pip install -r requirements.txt
```

## Run the code

All:

```bash
python main.py --mode all
```

Train:

```bash
python main.py --mode train
```

Test:

```bash
python main.py --mode test
```

You can overwrite the default configuration with command-line arguments. For example:

```bash
python main.py --mode test \
  --data_path ./data/pu_qrmc.npz \
  --checkpoint ./outputs/pu/checkpoints/best.pt \
  --run_dir ./outputs/pu \
  --observed_modalities VB,CU \
  --degraded_modalities VB \
  --snr_db 10
```
