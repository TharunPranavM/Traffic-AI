# 🚦 **Traffic Monitoring System**

## 📑 **Table of Contents**
- [About](#about)
- [Features](#features)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)

---
##🔹 Example Video: Real-Time Traffic Monitoring and ANPR in Action

https://github.com/user-attachments/assets/3552c06d-e2f3-4a8a-a581-89b8eeabfc65
---

## 📌 **About**
The Traffic Monitoring System is an AI-powered application designed to:
- Detect and count vehicles.
- Estimate their speed.
- Perform Automatic Number Plate Recognition (ANPR).
- Calculate the traffic rate based on video input.
- Provide real-time and recorded video processing options.

---

## ⚙️ **Features**
- **Vehicle Detection & Counting:** Uses YOLOv8 for accurate vehicle detection and counting.
- **Speed Estimation:** Estimates vehicle speeds using region-based tracking.
- **ANPR:** Recognizes license plates using OCR.
- **Traffic Rate Calculation:** Computes the traffic rate based on frame count and video duration.
- **Streamlit Interface:** Provides an intuitive and interactive web-based UI.

---

## 🔍 **How It Works**

1. **Input Source Selection:** 
    - Choose between **Live Video** (from a webcam) or **Recorded Video** (pre-recorded footage).

2. **Model Loading & Initialization:**
    - The system uses YOLOv8 for vehicle detection and a custom-trained YOLO model for license plate recognition.
    - It loads the model (`yolov8s.pt`) and defines tracking regions and counters.

3. **Video Processing:**
    - For live video, frames are processed continuously in real-time.
    - For recorded videos:
        - The system reads the video file frame by frame.
        - It detects and tracks vehicles.
        - It estimates speed and performs ANPR if selected.

4. **Data Processing & Display:**
    - Results such as vehicle count, speed, and license plate numbers are displayed on the Streamlit interface.
    - The processed video is saved and displayed in the output section.
    - The traffic rate is calculated using the frame count and duration.

5. **Output:**
    - The system generates a CSV file with the detected vehicles and license plate data.
    - The processed video is saved as `output.mp4`.

---

## ⚙️ **Installation**

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd traffic-monitoring-system
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Install YOLO models and dependencies:
   ```bash
   pip install ultralytics
   pip install opencv-python pandas numpy easyocr scipy moviepy
   ```

---

## 🚀 **Usage**

1. **Run the Streamlit App**
   ```bash
   streamlit run app.py
   ```

2. **Select Task Options**
    - Choose between **Live Video** or **Recorded Video**.
    - Select the desired task:
      - Vehicle Counting
      - Speed Estimation
      - ANPR

3. **Upload/Select Video**
    - For recorded videos, upload or select the desired file.
    - For live video, the webcam will automatically start streaming.

4. **Process & View Results**
    - View the detected vehicles, their speed, and license plate numbers.
    - The processed video is saved as `output.mp4`.

---

## 🛠️ **Technologies Used**
- **Programming Language:** Python
- **Framework:** Streamlit
- **Computer Vision:** OpenCV, YOLOv8
- **OCR:** EasyOCR
- **Data Processing:** Pandas, NumPy
- **Video Handling:** MoviePy

---

