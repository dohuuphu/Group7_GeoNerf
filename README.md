## Installation

#### Tested on GeForce RTX 3090 GPUs with PyTorch 1.9 and PyTorch Lightning 1.3.7

To install the dependencies, in addition to PyTorch, run:

```
pip install -r requirements.txt
```

## Download weight
To reproduce our results, download pretrained weights from [here](https://drive.google.com/drive/folders/1ZtAc7VYvltcdodT_BrUrQ_4IAhz_L-Rf?usp=sharing) and put them in [pretrained_weights](./pretrained_weights) folder.

## LLFF (Real Forward-Facing) Dataset
Download `nerf_llff_data.zip` from [here](https://drive.google.com/drive/folders/128yBriW1IG_3NJ5Rp7APSTZsJqdJdfc1) and set its path as `llff_path` in the [config_llff.txt](./configs/config_llff.txt) file.

1.  NonFinetune -evaluation: 
In [config_llff_fern.txt](./configs/config_llff.txt) file: 
- Set number of source view is 3 (nb_views = 3)
- Select sampling mode is  "baseline", "random", "spatial"
run the following command:
```
python run_geo_nerf.py --config configs/config_llff_fern.txt --eval
```

2.   Finetune evaluation:
```
python run_geo_nerf.py --config configs/config_llff_fern.txt
```
