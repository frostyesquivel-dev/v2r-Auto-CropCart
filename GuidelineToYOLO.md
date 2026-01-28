# Making model for grass classification using RPI5  
Always avtivate virtual environment and go into the ultralytics folder where it has yolov11n.pt installed already, so that it wont install in home folder.
```bash
source venv/bin/activate
```
```bash
cd yolo_project/ultralytics
```
```bash
yolo train model=yolo11n.pt data=/home/v2r-tank/yolo_project/ultralytics/cfg/datasets/coco8.yaml epochs=100 lr0=0.01 name=test
```
