# Tasks Summary

-The project successfully implemented object detection and segmentation using the YOLOv11 family of models (nano, small, and medium variants). 
-Model performance was found to correlate directly with size, with larger models achieving better results. 
-All output bounding boxes displayed the respective confidence scores.

##Object detection

```bash
yolo predict model=yolo11n.pt source=/Users/cheesecake/projai/images imgsz=640 conf=0.25 
```
This command runs Object Detection using the YOLOv11 nano model (yolo11n.pt) on the images found in the /Users/cheesecake/projai/images directory, using a minimum prediction confidence score of 0.25 and an input image size of 640 pixels.


input images:

/Users/cheesecake/projai/egs/eg2.jpg

/Users/cheesecake/projai/egs/eg1.jpg

output images:

/Users/cheesecake/projai/runs/detect/predict7-myEgs/eg1.jpg

/Users/cheesecake/projai/runs/detect/predict7-myEgs/eg2.jpg


##Segmentation

```bash
yolo predict model=yolo11n-seg.pt source=/Users/cheesecake/projai/images imgsz=640 conf=0.25 
```
This command will generate image outouts after segmentation, based on the object.

output images:

/Users/cheesecake/projai/runs/segment/predict2-myEgs/eg1.jpg

/Users/cheesecake/projai/runs/segment/predict2-myEgs/eg2.jpg

## Use of ffmpeg for video clip
FFmpeg is used to manage the input/output phases.

```bash
ffmpeg -i input.mp4 frame%d.jpg
ffmpeg -i runs/detect/predict2/frame%d.jpg mir.mp4
```
The first command extracts the original video clip into a sequence of individual image frames.
The second command puts together the processed sequence of frames (the output images with detections/segmentations) back into a single video file

video file input:

/Users/cheesecake/projai/mirs.mp4

video file output:

/Users/cheesecake/projai/mirl.mp4

/Users/cheesecake/projai/mirs_seg.mp4
