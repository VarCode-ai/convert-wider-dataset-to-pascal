# convert-wider-dataset-to-pascal
This repository is based on https://github.com/akofman/wider-face-pascal-voc-annotations but it converts the dataset according to YOLOX conventions.

You can download the whole [WIDER FACE](http://shuoyang1213.me/WIDERFACE/) datasets already converted in [Pascal VOC](http://host.robots.ox.ac.uk/pascal/VOC/) XML format. here: 

```
usage: convert.py [-h] [-ap ANNOTATIONS_PATH] [-tp TARGET_PATH]
                  [-ip IMAGES_PATH] [-t TYPE]

optional arguments:
  -h, --help            show this help message and exit
  -ap ANNOTATIONS_PATH, --annotations-path ANNOTATIONS_PATH
                        the annotations file path.
                        ie:"wider_face_train_bbx_gt.txt".
  -tp TARGET_PATH, --target-path TARGET_PATH
                        the target directory path where XML files will be
                        copied. ie:"Annotations"
  -ip IMAGES_PATH, --images-path IMAGES_PATH
                        the images directory path. ie:"./JPEGImages"
  
  -t TYPE, --type TYPE  the ImageSets name. ie:"train(default)/val/test"

```
It has been used as following:

```
python convert.py -ap wider_face_train_bbx_gt.txt -tp Annotations -ip ./JPEGImages/ -t train
python convert.py -ap wider_face_val_bbx_gt.txt -tp Annotations -ip ./JPEGImages/ -t val
```
# License

MIT Licensed. Copyright (c) Vincenzo Varriale 2022.
