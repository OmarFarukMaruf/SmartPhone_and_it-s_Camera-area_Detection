# SmartPhone_and_its_CameraArea_Detection
For security purposes in museums, the security cell adopts several strategies and live monitoring using CCTV is one of them. That monitoring video is used for the proposed model: Non-Permissible Mobile Detection in Museums (NMDM). Firstly, the model takes n frames per process from the monitoring video. By using those frames, the NMDM model will predict parallelly whether the object is detected (e.g. smartphone and camera area of the smartphone) or not. The proposed NMDM model is trained by the pre-trained You Only Look Once version 8 (YOLOv8) model. Finally, an ensemble technique is used to merge n individual detection results that help to decide on Non-Permissible Mobile Detection.

The system captures video at n frames per second by the CCTV in the museum and the corresponding frames are extracted in time sequence and the frames are sent to the automatic smartphone detection system (NMDM). This model will generate an alarm to aware the museum security supportive cell.
<img width="242" alt="image" src="https://github.com/OmarFarukMaruf/SmartPhone_and_its_CameraArea_Detection/assets/92799144/e541e50e-3c06-425b-9bb6-2323a96f2613">

# Data Augmentation
The image dataset is adjusted before training to a size of 640 × 640. Rotate the images left 900 and right 900 to improve the robustness of the NMDM model in a real-time scenario. Then the data was enhanced with five distinct factors: gauss noise, random rain, hue saturation value, random brightness contrast, and blur. Finally, a total of 583 mobile images of phone brands became 10494.
<img width="246" alt="image" src="https://github.com/OmarFarukMaruf/SmartPhone_and_its_CameraArea_Detection/assets/92799144/eabf9bf5-e2d2-4624-83fa-3e483b2cf9c1">


# Training Process
The model is trained and tested using the augmented data using a 5-fold Cross-Validation technique. We assigned labels to each object to apply the NMDM model to our customized dataset under our particular needs. Using the web annotation tool CVAT.AI, we produced two labels: "phone" and "camera”.In each iteration, we allocate five folds in a total of 8395 images (80% of the custom dataset) for training and the remaining one-fold is for testing in a total of 2099 images (20% of the custom dataset) by cross-validation technique. Here evaluate 50 epochs for each set of hyper-parameters as an indicator of the potential performance of additional epochs.


# Reselt
NMDM test confusion matrix for fold-4:

The proposed NMDM model is tested using different system configurations (Multi-Process CPU and GPU with 4GB) through a 10m video. Where the GPU system is 54.56% (e.g., (158.98 ÷ 291.34) ×100)faster than the CPU.




To detect any object with custom data, here are the steps to do:

# Step 01
Download the repository and run the detection.py file.
This file is for mounting the drive, and training the dataset with yolov8 (Here we use the yolov8n.pt model)



Dataset link: https://drive.google.com/drive/folders/1s3EYq2U19Z7uyy09dyWd1jKYyelg-tkd?usp=sharing
