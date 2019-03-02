# Pix2pix+DRPAN in PyTorch

This is our PyTorch implementation of Pix2pix+DRPAN on image-to-image translation.

## Prerequisites
- Linux or OSX.
- Python 2 or Python 3.
- CPU or NVIDIA GPU + CUDA CuDNN.

## Getting Started
### Installation
- Install PyTorch and dependencies from http://pytorch.org/.
- Install python libraries [dominate](https://github.com/Knio/dominate).
```bash
pip install dominate
```

- Clone this repo:
```bash
git clone https://github.com/godisboy/DRPAN/Pix2pix_DRPAN.git
cd Pix2pix_DRPAN
```
- Prepare your paired image2image translation dataset.

- Modify the config file:
change the `dataPath` to your data set path.

### Pix2pix+DRPAN train/test
- Train a model:
```
python main.py --config configs/cityscapes.yaml --cuda --gpu_ids 0

```
The train results and trained model will be saved to `checkpoints`, you can set the `outf` in config file.
- Test a model:
```
python test.py --config configs/cityscapes.yaml --checkpoints/generator_epoch_200.pkl--cuda --gpu_ids 0

```
If you want to test with the trained model of other epochs, please modify `--checkpoints/generator_epoch_other.pkl`. 