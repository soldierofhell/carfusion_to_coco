# CarFusion: Combining Point Tracking and Part Detection for Dynamic 3D Reconstruction of Vehicle

[N Dinesh Reddy](http://cs.cmu.edu/~dnarapur), [Minh Vo](http://www.cs.cmu.edu/~mvo), [Srinivasa G. Narasimhan](http://www.cs.cmu.edu/~srinivas/)

IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2018. 

[[Project](http://www.cs.cmu.edu/~ILIM/projects/IM/CarFusion/)] [[Paper](http://www.cs.cmu.edu/~ILIM/publications/PDFs/RVN-CVPR18.pdf)] [[Supp](http://www.cs.cmu.edu/~ILIM/projects/IM/CarFusion/pdf/occlusion_net_supp.pdf)]

## Requirements
- Python 3.6
- Virtualenv
- OpenCV 
- Numpy
- Glob
- googledrivedownloader
- shapely
- Cython

## Setup
To download the data and  convert it to coco format using the following commandse
```
virtualenv carfusion2coco -p python3.6
source carfusion2coco/bin/activate
pip install cython numpy
pip install -r requirements.txt
sh carfusion_coco_setup.sh
```
## Dataset((14 Keypoints annotations for 100,000 cars(53,000 Images)))

We provide mannual annotations of 14 semantic keypoints for 100,000 car instances (sedan, suv, bus, and truck) from 53,000 images captured from 18 moving cameras at Multiple intersections in Pittsburgh, PA. To view the labels, please run the following command:

## To visualize the data
Visualization of the carfusion original labels
```
python Visualize.py PathToData CamID_FrameID
```

For example:
```
python Visualize.py ./datasets/carfusion/train/car_butler1/ 16_06401
```


Visualization of the coco format labels

```
python visualize_carfusion_coco.py
```

