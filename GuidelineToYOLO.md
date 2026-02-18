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
```bash
yolo predict model=/home/v2r-tank/yolo_project/ultralytics/runs/detect/test2/weights/best.pt source=0 show=True //the source=0 represents for example the camera

```
to check what your source is for cameras used on usb connections, do this lne of code and see what camera is what for each source
```bash
v4l2-ctl --list-devices
```


```bash
yolo train model=yolo11n.pt data="/home/jonahesq/ultralytics/CROPCART=aerial-data-3/data.yaml" epochs=50 imgsz=416 batch=16 device=cpu
```
