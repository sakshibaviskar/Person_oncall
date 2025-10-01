# 📱 Smart Person-on-Call Detection System (YOLO Powered)

![Detection Example](assets/detection_example.png)

---

## 📝 Project Overview

The **Smart Person-on-Call Detection System** is an intelligent **real-time phone usage detection** solution powered by a **YOLO object detection model**.  

It continuously analyzes a video stream and automatically detects when a person is talking on a mobile phone, even in indoor or casual environments.  

When a phone-usage event is detected, the system:

- Draws a **bounding box** around the person  
- Shows a **confidence score**  
- **Crops and saves** the detected frame for logging or evidence  
- Updates a **live counter** of total detected 'on-call' events  

> **Prototype Note:** The current demo uses a sample video (`sample_video.mp4`), but you can replace it with any CCTV or recorded video.

---

## ✨ Key Features

- **Real-time detection** of people using a mobile phone (YOLO model – `best.pt`)  
- **Annotated video output** with bounding boxes and confidence values  
- **Automatic cropping & saving** of violation frames  
- **Live event counting** and time-based logging  
- **Easily customizable** for different environments or use cases  

---

## 📷 Demonstration / Output Example

Here’s an example of the system detecting a person 'on call':

![Detection Example](assets/detection_example.png)

---

## 📂 Project Structure

Person-On-Call-Detection/
├── main.py # Main detection script
├── best.pt # YOLO weights for phone detection
├── sample_video.mp4 # Input video (replace with your own)
├── training.ipynb # (Optional) Notebook used to train the model
├── README.md # Project documentation
└── assets/
└── detection_example.png # Example output image


---

## ⚙️ Installation Instructions

```bash
git clone https://github.com/<your-username>/person-on-call-detection.git
cd person-on-call-detection
pip install ultralytics opencv-python numpy
