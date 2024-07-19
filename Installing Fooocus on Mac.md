---
publish: "true"
---

Local image generation on Apple Silicon

Instructions based on Mac install guide found here: https://github.com/lllyasviel/Fooocus?tab=readme-ov-file
#### Install Miniconda
```
curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh
sh Miniconda3-latest-MacOSX-arm64.sh
```
#### Refresh Shell
```
source ~/.zshrc
```
#### Install PyTorch
```
conda install pytorch torchvision torchaudio -c pytorch-nightly
```
#### Git Clone Fooocus
```
git clone https://github.com/lllyasviel/Fooocus.git
```
#### Enter Directory
```
cd Fooocus
```
#### Create New Conda Environment
```
conda env create -f environment.yaml
```
#### Activate New Conda Environment
```
conda activate fooocus
```
#### Install Fooocus Dependencies
```
pip install -r requirements_versions.txt
```
#### Launch Fooocus
(First start will download Stable Diffusion SDXL which are large and takes a long time)
```
python entry_with_update.py --disable-offload-from-vram
```
