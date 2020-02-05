# RCNN implimentation

Computer vision as we know always move around classification and object detection and hence discussing some of the early breakthroughs are pretty sure helpful in understanding modern research. R-CNN was one of the first approach to discuss detection through convolution. Instead of using huge number of proposals R-CNN uses only first 2000 of them, which make it faster than other approches available at that time. 

## Getting Started

Using this notebook is quite simple, you have to just open it and set directory to your google drive with data loaded in it. Running individual cells afterward will easily impliment our network.

## Network

let's discuss it in steps-
1. First step- Running selective search on indvidual image to obatain region proposals(2000 here).
2. Second step- Classifying region proposals as positive and negative example based on IOU(IOU explained properly in notebook itself).
3. Third step- Passing every proposal through pretrained network on some image dataset(We use VGG 16 trained on ImageNet) to output a fixed size feature vecotr(4096 here).
4. Fourth step- Using this feature vector to train a SVM.
5. Fifth step- Use bounding box regression for more accurate results(We haven't done it here).

Note- Hyperparamters were not tunned properly because the work is not to show the acccuracy but to make you aware about implimentation of R-CNN. 

So,finally it will give you idea of R-CNN with implimentaion for better understanding.
