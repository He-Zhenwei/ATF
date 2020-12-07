# ATF
The code of our ECCV paper: Domain Adaptive Object Detection via Asymmetric Tri-way Faster-RCNN

The code is based on the Pytorch 0.4.0.
For training our model for Cityscapes and Foggy Cityscapes datasets:

python da_trainval_net.py 
--dataset cityscape
--net vgg16
--save_dir ./output/da_model
--epochs 14
--bs 1
--lr 1e-3
--lr_decay_step 10
--cuda

For testing out model:

python ./eval/test.py 
--dataset cityscape
--net vgg16
--part test_t
--model_dir ./output/da_model/vgg16/cityscape/cityscape_1_13.pth
--cuda
