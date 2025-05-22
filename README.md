# **Head Pose Controlled Interface - README**

## **Project Overview**
This project implements a **hands-free interface** that detects head movements (nods for "YES" and shakes for "NO") to answer questions. It uses **MediaPipe Face Mesh** for real-time head pose estimation and **OpenCV** for camera input and display.

---

## **Features**
1. **Head Pose Estimation** – Detects 3D head orientation (pitch, yaw, roll).
2. **Gesture Recognition** – Classifies nods (YES) and head shakes (NO).
3. **Interactive Q&A System** – Displays questions and registers answers via head movements.
4. **Calibration System** – Ensures accurate gesture detection by establishing a neutral head position.

---

## **Setup Instructions**
### **Prerequisites**
- Python 3.7+
- Webcam
- Stable lighting conditions

### **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/head-pose-interface.git
   cd head-pose-interface
   ```
2. Install dependencies:
   ```bash
   pip install opencv-python mediapipe numpy
   ```
3. Run the application:
   ```bash
   python head_pose_interface.py
   ```

---

## **How to Use**
### **1. Calibration**
- **When starting**, the system will automatically calibrate.
- **Hold your head steady** while the progress bar fills (takes ~2 seconds).  
   ![Calibration Screen](https://github.com/Jaifin-aloor/MMP-1/blob/main/Screenshot%202025-05-22%20103302.png)  
   *(Example: User holding head straight for calibration)*

### **2. Answering Questions**
- **Nod DOWN** (pitch change) → **"YES"**  
   ![Nod Detection](https://github.com/Jaifin-aloor/MMP-1/blob/main/Screenshot%202025-05-22%20103313.png)
   *(Example: User nodding downward for "YES")*
- **Shake LEFT/RIGHT** (yaw change) → **"NO"**  
   ![Shake Detection](https://github.com/Jaifin-aloor/MMP-1/blob/main/Screenshot%202025-05-22%20103218.png)
   *(Example: User shaking head for "NO")*
- **Press `SPACE`** to confirm your answer.  

### **3. Manual Recalibration**
- Press **`C`** at any time to recalibrate if detection is inaccurate.

### **4. Quitting**
- Press **`Q`** to exit the application.

---

## **Troubleshooting**
- **Issue:** False detections  
  **Fix:** Ensure proper lighting and recalibrate (`C` key).
- **Issue:** Camera not working  
  **Fix:** Check webcam permissions or try another camera.
- **Issue:** MediaPipe errors  
  **Fix:** Reinstall dependencies (`pip install --upgrade mediapipe`).

