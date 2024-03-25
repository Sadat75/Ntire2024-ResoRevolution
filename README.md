# Modified HAT-L Reference 
https://dacon.io/en/competitions/official/235977/codeshare/6908?page=1&dtype=recent
https://dacon.io/en/competitions/official/235977/codeshare/6901?page=1&dtype=recent

## HAT Reference
- HAT [[Paper Link]](https://arxiv.org/abs/2205.04437)
- HAT [[Code Link]](https://github.com/XPixelGroup/HAT)
- HAT-Pretrained Model - check Training section

## Environment Requirements
- Python == 3.8
- [PyTorch == 2.1.1](https://pytorch.org/)
- [BasicSR == 1.3.4.9](https://github.com/XPixelGroup/BasicSR/blob/master/INSTALL.md)

### Installation
Please follow the instructions below to setup the environment.

## Install depedencies
```
conda create -n HAT python=3.8
conda activate HAT
conda install pytorch==2.1.1 torchvision==0.16.1 torchaudio==2.1.1 pytorch-cuda=11.8 -c pytorch -c nvidia
pip install -r requirements.txt
python setup.py develop
```

## How To Test

- Refer to `./options/test.yml` for the configuration file of the model to be tested, and prepare the testing data and pretrained model.  

- Download model to `./model_zoo/team11_hat.pth`

- Then run the follwing codes to reproduce submission results:

```
CUDA_VISIBLE_DEVICES=0 python hat/test.py -opt options/test.yml
```

The testing results will be saved in the `./results` folder.

## Results
The inference results will be saved under `results/modelname/visualization` folder
