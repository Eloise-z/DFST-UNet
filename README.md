# DFST-UNet

This is the official code for our paper (xxxxxxx). Please note that the code is still being organized, and this is just a rough framework.

## 1. Environment
We use conda to manage the environment with Python 3.8 and PyTorch 1.12. Detailed environment configurations can be found in `requirements.yaml`, which is an exported conda environment file. However, it includes some non-essential libraries that do not affect functionality. You can install the entire configuration directly, or selectively install only the essential packages such as Python, PyTorch, NumPy, and OpenCV.

## 2. Dataset
We provide a dataset class to load `.txt` files that describe dataset information. Each line in the `.txt` file contains `img_path # gt_mask_path # cls`. The class loads the dataset based on the dataset name during initialization, which reads the corresponding `.txt` file, rather than passing the dataset path directly.

## 3. Train
We provide `train.py`. You will need to download the weights provided by Swin-UNet and place them in the `pretrained_ckpt` folder. Modify some configurations in `train.py` according to your local environment, such as the model save path.

## 4. Test
We provide the pre-trained weights used in our experiments. You can directly run `test_sample.py` to visualize the output of our model.

## References
* [Swin-Unet](https://github.com/HuCaoFighting/Swin-Unet)