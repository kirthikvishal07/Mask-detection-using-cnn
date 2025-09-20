# 🩺 Real-Time Face Mask Detection

This project detects whether a person is wearing a mask 😷 or not 🙅 in real-time video streams using a pre-trained deep learning model.

## 📂 File Structure
```bash
Facemask Detection Project/
│── dataset/ # Dataset used (already included)
│── face_detector/ # Pre-trained Face Detection model (Caffe)
│ ├── deploy.prototxt
│ ├── res10_300x300_ssd_iter_140000.caffemodel
│── mask_detector.h5 # Pre-trained Mask Classification model
│── Main_file_videoStream_maskDetection.ipynb # Run real-time mask detection
│── Video_Based_Facemask_Detection_Model_Creation.ipynb # (Optional) training notebook
│── plot.png # Training performance graph
```
## 🚀 How to Run

### 1. Real-Time Detection
Run the following notebook:
```bash
jupyter notebook Main_file_videoStream_maskDetection.ipynb
This will:
  Start the webcam
  Detect faces (using deploy.prototxt + .caffemodel)
  Predict mask/no-mask (using mask_detector.h5)
  Show live video with bounding boxes and labels
```
### 2. Re_train the model (optional)
```bash
If you want to train the mask classifier again:
jupyter notebook Video_Based_Facemask_Detection_Model_Creation.ipynb
This will recreate mask_detector.h5 using the dataset provided.
```
### 3. For dataset visit kaggle 
```bash
https://www.kaggle.com/datasets/omkargurav/face-mask-dataset
```

## 🔄 Workflow
```bash
Face Detection → Locate faces in each video frame
Preprocessing → Crop, resize, and normalize the face
Mask Classification → Classify each face as Mask or No Mask
Display → Show live video feed with results
```

