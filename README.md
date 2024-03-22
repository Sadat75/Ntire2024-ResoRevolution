# HAT-L 모델 


## Reference
- HAT [[Paper Link]](https://arxiv.org/abs/2205.04437)
- HAT [[Code Link]](https://github.com/XPixelGroup/HAT)
- HAT-Pretrained Model - check Training section


## Environment
- [PyTorch >= 1.7](https://pytorch.org/)
- [BasicSR == 1.3.4.9](https://github.com/XPixelGroup/BasicSR/blob/master/INSTALL.md)

### Installation

## Install depedencies
```
pip install -r requirements.txt
```

## How To Test

- Refer to `./options/test.yml` for the configuration file of the model to be tested, and prepare the testing data and pretrained model.  

- Download model to `experiments/pretrained_models/team11_hat.pth`

- Then run the follwing codes to reproduce submission resulsts
```
CUDA_VISIBLE_DEVICES=0 python hat/test.py -opt options/test.yml
```
The testing results will be saved in the `./results` folder.

## Results
The inference results will be saved under `results/modelname/visualization` folder
