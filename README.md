MFF
# Multi-Dimensional Feature Fusion and Layer-interactive Attention Reinforced for Inslulator Detection in Remote Sensing Imagery

Installation
Use git clone https://github.com/ultralytics/yolov5/tree/v5.0 to clone the project,the code modification is based on yolov5s, the dataset concluded train set and test set and the pre-training weightis in the direction weight. For training of other models, please refer to mmdetection. We have uploaded all the information related to the project to the folder.


## Introduction
Insulators play a pivotal role in high-voltage transmission lines, and their condition monitoring becomes an important part of maintaining the stability of the power system.... For more details, please refer to our [paper]().

## Installation
Use `git clone https://github.com/ultralytics/yolov5/tree/v5.0`
to clone the project,the code modification is based on yolov5x,
the [insulator_dataset](https://pan.baidu.com/s/1uZY8DCeKm-mn6u-EiBp00A?pwd=1234) concluded train set and test set, due to the large capacity of the training set, we split four small files, train_images1,train_images2,train_images3 and train_images4.
and the [pre-training weight](https://pan.baidu.com/s/1LyqiE-DJzFtThRe3hLv5Pg?pwd=1234)is in the direction `weight`.

## Training
You can use the following commands for training:

    python train.py --device 'your device' 
                    --datapath 'your path of dataset' 
                    --num-classes 'number of detected categories (excluding background)'
                    --output_dir 'path where to save log' 
                    --resume 'pre-training weights' 
                    --start-epoch 'start epoch'
                    --epoch 'number of total epochs to run' 
                    --batch_size 'batch size when training'
    
such as:

    python train.py --device 'cuda:0' \
                    --datapath './data' \
                    --num-classes 2 \
                    --output_dir './save_weights' \
                    --resume './pre_training_weights/your_weights.pth' \
                    --epoch 300 \
                    --batch_size 16
