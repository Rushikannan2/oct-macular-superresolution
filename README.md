<<<<<<< HEAD
# OCT Image Reconstruction using Variational Autoencoder (VAE)

This project implements a Variational Autoencoder (VAE) for grayscale OCT image reconstruction using PyTorch.

The entire pipeline runs locally and includes:

- image preprocessing
- dataset splitting
- PyTorch dataset loader
- VAE training
- validation
- checkpointing
- reconstruction preview
- evaluation

No Kaggle or Colab required.

---

## Project Pipeline

```
raw_png
   ↓ preprocessing
processed_png
   ↓ dataset split
dataset/train | val | test
   ↓
PyTorch DataLoader
   ↓
VAE training + evaluation
```

---

## Folder Structure

```
project/
│
├── raw_png/               # original OCT images
├── processed_png/         # resized images
├── dataset/
│   ├── train/
│   ├── val/
│   └── test/
│
├── vae_outputs/           # training outputs
│   ├── previews/
│   └── checkpoints
│
├── notebook.ipynb
├── requirements.txt
└── README.md
```

---

## Python Version

Recommended:

```
Python 3.10 or 3.11
```

Do NOT use Python 3.12 yet.

---

## Installation (CPU version)

```
pip install torch==2.2.2 torchvision==0.17.2 --index-url https://download.pytorch.org/whl/cpu
pip install -r requirements.txt
```

---

## Installation (GPU version – CUDA 12)

```
pip install torch==2.2.2 torchvision==0.17.2 --index-url https://download.pytorch.org/whl/cu121
pip install -r requirements.txt
```

---

## How to Run

1. Put raw OCT images inside:

```
raw_png/
```

2. Run preprocessing section  
→ creates `processed_png`

3. Run dataset split  
→ creates `dataset/train/val/test`

4. Run training section  
→ saves model in `vae_outputs`

5. Run test section  
→ shows reconstruction results

---

## Model Details

- Input size: 512 × 512 grayscale
- Latent channels: 8
- Symmetric encoder-decoder architecture
- Loss: L1 + KL divergence
- Mixed precision supported on GPU
- Resume training supported

---

## Output

Training produces:

- epoch preview images
- best model checkpoint
- resume checkpoint
- validation metrics

All saved in:

```
vae_outputs/
```

---

## Compatibility

- Windows ✔
- Linux ✔
- macOS ✔
- CPU ✔
- GPU ✔

---

## Notes

- No cloud dependency
- Notebook-safe paths
- Portable project
- Stable library versions

---

## Author

Student project – OCT VAE pipeline
=======
# OCT Macular Super-Resolution

This project applies deep learning techniques to enhance the resolution of macular OCT retinal images.

## Objective
To improve visualization of the posterior segment (retina) using super-resolution methods for medical imaging.

## Methods Tried
- GAN-based super-resolution (ex: SRGAN, ESRGAN)
- Diffusion-based methods (planned or optional)

## Dataset
Heidelberg Spectralis OCT dataset (Posterior Segment - Retina)

## Tools and Frameworks
- Python
- PyTorch
- OpenCV

## Expected Outcome
Higher resolution macular OCT images suitable for clinical or research analysis.
>>>>>>> 7d8e9ae5c5c70d9531c5f2be4878f54a5d948b60
