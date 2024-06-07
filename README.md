# SmartPhone_and_its_CameraArea_Detection
For security purposes in museums, the security cell adopts several strategies and live monitoring using CCTV is one of them. That monitoring video is used for the proposed model: Non-Permissible Mobile Detection in Museums (NMDM) which is illustrated in Figure 1. Firstly, the model takes n frames per process from the monitoring video. By using those frames, the NMDM model will predict parallelly whether the object is detected (e.g. smartphone and camera area of smartphone) or not. The proposed NMDM model is trained by the pre-trained You Only Look Once version 8 (YOLOv8) model that is described in Section (IV.B). Finally, an ensemble technique is used to merge n individual detection results that help to decide on Non-Permissible Mobile Detection.![image](https://github.com/OmarFarukMaruf/SmartPhone_and_its_CameraArea_Detection/assets/92799144/64549742-f972-4597-9496-12a4b3f88f94)

The system captures video at n frames per second by the CCTV in the museum and the corresponding frames are extracted in time sequence and the frames are sent to the automatic smartphone detection system (NMDM) which is depicted in Figure 2. This model will generate an alarm to aware the museum security supportive cell.![image](https://github.com/OmarFarukMaruf/SmartPhone_and_its_CameraArea_Detection/assets/92799144/c7120c0e-4886-4356-8dbe-4740111a957f)

To detect any object with custom data, here are the steps to do:

# Step 01
Download the repository and run the detection.py file.
This file is for mounting the drive, and training the dataset with yolov8 (Here we use the yolov8n.pt model)



Dataset link: https://drive.google.com/drive/folders/1s3EYq2U19Z7uyy09dyWd1jKYyelg-tkd?usp=sharing
