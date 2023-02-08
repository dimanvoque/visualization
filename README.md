# Visualization of Convolutional Neural Networks for Monocular Depth Estimation (KITTI Odometry Dataset)

============================

This repo offers a masks' visualization pipeline for KITTI Odometry Dataset 

## Downloading the models 

Download the trained encoder  : https://drive.google.com/drive/folders/1ZGwumOViQr6oECQfN4NLtT1jfljFrgAf?usp=sharing

Download the mask prediction network : https://drive.google.com/drive/folders/1aivLjv_-p4k6zkppgBSso1dWvZO0R7AE?usp=sharing

## Dataset 

The repo contains several samples of the KITTI Odometry dataset.

If you want to download the whole KITTI Odometry dataset, please run the following command:

```bash
mkdir kitti; cd kitti
wget http://datasets.lids.mit.edu/sparse-to-dense/data/kitti.tar.gz
tar -xvf kitti.tar.gz && rm -f kitti.tar.gz
cd ..
```

## Masks' inference

To get the masks, you should run the following command: 
```bash
python main.py --evaluate results/kitti.samples=0.modality=rgb.arch=MobileNetSkipAdd.decoder=nnconv.criterion=l1.lr=0.01.bs=8.pretrained=True/model_best.pth.tar
```
