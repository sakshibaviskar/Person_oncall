# Person_oncall
📞 Smart Person-on-Call Detection System (YOLO Powered)

This project demonstrates an intelligent real-time Person-on-Call Detection System, powered by a YOLO object detection model.
It continuously analyzes each frame of a video stream and automatically detects when a person is talking on a mobile phone even in indoor or casual environments.

When a phone-usage event is detected, the system:

✅ Draws a bounding box around the detected person
✅ Shows a confidence score in real time
✅ Crops and saves the detected frame for logging / evidence
✅ Updates a live counter of total detected “on-call” events

⚠️ Prototype Note:
The current demo uses a sample video, however you can simply replace it with any CCTV or recorded video (office, classroom, public area, etc.) to test it in a real-world scenario.

✅ Features

🔍 Real-time detection of people using a mobile phone (YOLO model – best.pt)

 Annotated video output with bounding boxes and confidence values

 Automatic cropping & saving of violation frames

 Live event counting and time-based logging

 Easily customizable for different environments or use cases

📂 Project Structure
Person-On-Call-Detection/
├── main.py                # Main detection script
├── best.pt                # YOLO weights for phone detection
├── sample_video.mp4       # Input video (replace with your own)
├── training.ipynb         # (Optional) Notebook used to train the model
└── README.md              # Project documentation

🔧 Installation
git clone https://github.com/<your-username>/person-on-call-detection.git
cd person-on-call-detection
pip install ultralytics opencv-python numpy

📥 Add Your Files
File	Description
best.pt	Trained YOLO weights for person-on-call detection
sample_video.mp4	Input video for detection (can be replaced with any video file)
🚀 Usage
python main.py


➡️ Press Q at any time to stop and exit.

⚙️ Customization (in main.py)
Parameter	Description
frame_skip	Skip frames to improve speed (lower = smoother)
CONF_THRESHOLD	Minimum confidence required for a valid detection
save_crop	Whether to save cropped detections (True or False)

Example:

frame_skip = 2
CONF_THRESHOLD = 0.35
save_crop = True

📊 Output
Output Item	Description
detections/	Cropped frames of detected phone-usage events
Annotated_Video.mp4	Output video with bounding boxes and confidence overlays
Console / Terminal	Real-time logs of detection events
📜 Disclaimer

This project is intended for educational and research purposes only.
If used in real environments, please ensure full compliance with local data privacy and surveillance regulations.
