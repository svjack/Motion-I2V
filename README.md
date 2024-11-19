# Motion-I2V Setup Guide

This guide will help you set up the Motion-I2V environment and run the application.

## Steps to Set Up and Run Motion-I2V

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/svjack/Motion-I2V
   cd Motion-I2V
   ```

2. **Create and Activate the Conda Environment:**
   ```bash
   conda env create -f env_edit.yaml
   conda activate motioni2v
   ```

3. **Install Required Packages:**
   ```bash
   pip install ipykernel "httpx[socks]"
   ```

4. **Install the IPython Kernel:**
   ```bash
   python -m ipykernel install --user --name motioni2v --display-name "motioni2v"
   ```

5. **Clone the Model Repository:**
   ```bash
   git clone https://huggingface.co/wangfuyun/Motion-I2V
   cp -r Motion-I2V/models models
   ```

6. **Run the Application:**
   ```bash
   python -m scripts.app
   ```

## Additional Notes

- Ensure you have Conda installed on your system before proceeding with the setup.
- The `env_edit.yaml` file contains the necessary dependencies for the environment.
- The `motioni2v` environment will be used to run the application.

Feel free to reach out if you encounter any issues during the setup process.

## Backwards-moving car example

![car](https://github.com/user-attachments/assets/9a180b4d-2846-45ec-8b65-2803e58193bf)


![image](https://github.com/user-attachments/assets/f801b78b-9fd9-4c49-935e-870b7cfd5452)


<div align="center">

## Motion-I2V: Consistent and Controllable Image-to-Video Generation with Explicit Motion Modeling
by *Xiaoyu Shi<sup>1\*</sup>, Zhaoyang Huang<sup>1\*</sup>, Fu-Yun Wang<sup>1\*</sup>, Weikang Bian<sup>1\*</sup>, Dasong Li <sup>1</sup>, Yi Zhang<sup>1</sup>, Manyuan Zhang<sup>1</sup>, Ka Chun Cheung<sup>2</sup>, Simon See<sup>2</sup>, Hongwei Qin<sup>3</sup>, Jifeng Dai<sup>4</sup>, Hongsheng Li<sup>1</sup>* 

*<sup>1</sup>CUHK-MMLab   <sup>2</sup>NVIDIA   <sup>3</sup>SenseTime  <sup>4</sup>  Tsinghua University*
</div>



```bib
@article{shi2024motion,
            title={Motion-i2v: Consistent and controllable image-to-video generation with explicit motion modeling},
            author={Shi, Xiaoyu and Huang, Zhaoyang and Wang, Fu-Yun and Bian, Weikang and Li, Dasong and Zhang, Yi and Zhang, Manyuan and Cheung, Ka Chun and See, Simon and Qin, Hongwei and others},
            journal={SIGGRAPH 2024},
            year={2024}
            }
}
```



<div style="text-align: center;">
  <img src="./assets/motion-i2v.png" alt="Image description" title="motion-i2v" style="width: 100%; height: auto;">
            Overview of Motion-I2V. The first stage of Motion-I2V targets at deducing the motions that can plausibly animate
the reference image. It is conditioned on the reference image and text prompt, and predicts the motion field maps between
the reference frame and all the future frames. The second stage propagates reference image’s content to synthesize frames. A
novel motion-augmented temporal layer enhances 1-D temporal attention with warped features. This operation enlarges the
temporal receptive field and alleviates the complexity of directly learning the complicated spatial-temporal patterns.
</div>


## Usage

1. Install environments
```shell
conda env create -f environment.yaml
```
2. Download models
```shell
git clone https://huggingface.co/wangfuyun/Motion-I2V
```
3. Run the code
```shell
python -m scripts.app 
```

## ComfyUI

[ComfyUI-IG-Motion-I2V](https://github.com/IDGallagher/ComfyUI-IG-Motion-I2V)

![arch](https://github.com/IDGallagher/ComfyUI-IG-Motion-I2V/blob/main/assets/screenshot1.png)
