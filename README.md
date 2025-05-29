#this command is to stop last training
set KMP_DUPLICATE_LIB_OK=TRUE

#go back the train and val dataset where u put 
cd /d "path u save the training data"

# start train
yolo train model="yolo11n.pt" data="data.yaml" epochs=50 imgsz=640 device=cpu 

# get the visualized graphs
python visualize_yolo_labels.py

