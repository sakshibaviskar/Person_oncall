# Person_oncall

📞 Smart Person-on-Call Detection System (YOLO Powered)<br>
This project demonstrates an intelligent real-time Person-on-Call Detection System, powered by a YOLO object detection model.<br>
It continuously analyzes each frame of a video stream and automatically detects when a person is talking on a mobile phone even in indoor or casual environments.<br><br>

When a phone-usage event is detected, the system:<br>
✅ Draws a bounding box around the detected person<br>
✅ Shows a confidence score in real time<br>
✅ Crops and saves the detected frame for logging / evidence<br>
✅ Updates a live counter of total detected “on-call” events<br><br>

⚠️ Prototype Note: The current demo uses a sample video, however you can simply replace it with any CCTV or recorded video (office, classroom, public area, etc.) to test it in a real-world scenario.<br><br>

✅ Features<br>
🔍 Real-time detection of people using a mobile phone (YOLO model – best.pt)<br>
Annotated video output with bounding boxes and confidence values<br>
Automatic cropping & saving of violation frames<br>
Live event counting and time-based logging<br>
Easily customizable for different environments or use cases<br><br>

📂 Project Structure<br>
Person-On-Call-Detection/<br>
├── main.py                # Main detection script<br>
├── best.pt                # YOLO weights for phone detection<br>
├── sample_video.mp4       # Input video (replace with your own)<br>
├── training.ipynb         # (Optional) Notebook used to train the model<br>
└── README.md              # Project documentation<br><br>

🔧 Installation<br>
git clone https://github.com/&lt;your-username&gt;/person-on-call-detection.git<br>
cd person-on-call-detection<br>
pip install ultralytics opencv-python numpy<br><br>


🚀 Usage<br>
python main.py<br>
➡️ Press Q at any time to stop and exit.<br><br>

⚙️ Customization (in main.py)<br>
Parameter — Description<br>
frame_skip — Skip frames to improve speed (lower = smoother)<br>
CONF_THRESHOLD — Minimum confidence required for a valid detection<br>
save_crop — Whether to save cropped detections (True or False)<br><br>

Example:<br>
frame_skip = 2<br>
CONF_THRESHOLD = 0.35<br>
save_crop = True<br><br>

📊 Output<br>
Output Item — Description<br>
detections/ — Cropped frames of detected phone-usage events<br>
Annotated_Video.mp4 — Output video with bounding boxes and confidence overlays<br>
Console / Terminal — Real-time logs of detection events<br><br>

