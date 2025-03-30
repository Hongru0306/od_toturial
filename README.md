# od_toturial
This is the toturial repo for od.

## 1. Create env.
```
conda create -n yolo python=3.11
```

## 2. prepare env.
```
pip install -e .
```

## 3.Download the model.
```
https://github.com/ultralytics/assets/releases/download/v8.3.0/yolo11s.pt
```

## 4.Inference the model.
```
import warnings
warnings.filterwarnings('ignore')
from ultralytics import YOLO


if __name__ == '__main__':
    model = YOLO(r'E:\Paper\demo\ultralytics-main\yolo11s.pt') # select your model.pt path
    model.predict(source='dataset/images/test',
                  imgsz=640,
                  project='runs/detect',
                  name='exp',
                  save=True,
                  # conf=0.2,
                  # iou=0.7,
                  # agnostic_nms=True,
                  # visualize=True, # visualize model features maps
                  # line_width=2, # line width of the bounding boxes
                  # show_conf=False, # do not show prediction confidence
                  # show_labels=False, # do not show prediction labels
                  # save_txt=True, # save results as .txt file
                  # save_crop=True, # save cropped images with results
                )
```
## Analysis the inference results.
