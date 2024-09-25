# Volume Control Using Hand Gestures

### Overview
This capstone project demonstrates how to use **computer vision** and **hand tracking** to control the system volume using simple **hand gestures**. By utilizing a live camera feed, the system detects the distance between the user's thumb and index finger to adjust the volume level in real time. This project combines **MediaPipe**, **OpenCV**, and **PyCaw** libraries for efficient hand landmark detection and interaction with the system's audio controls.

### 🚀 Features
- **Real-time Hand Detection**: Detects hand landmarks using MediaPipe.
- **Gesture-Based Volume Control**: Adjusts volume based on the distance between the thumb and index finger.
- **Visual Feedback**: Displays volume percentage and visualizes volume changes with dynamic bars.
- **Smooth Performance**: Works with high precision and minimal lag.

### 🛠 Technologies Used
- **OpenCV**: For camera feed capture and image processing.
- **MediaPipe**: For real-time hand and finger tracking.
- **PyCaw**: For accessing and controlling the system's audio volume.
- **NumPy**: For mathematical calculations like distance measurement.

### 📋 Prerequisites
Before running the project, ensure you have the following:
- **Python 3.x**
- Required Python libraries:
  - `opencv-python`
  - `mediapipe`
  - `numpy`
  - `pycaw`
  - `comtypes`

You can install these dependencies by running:
```bash
pip install opencv-python mediapipe numpy pycaw comtypes
```

### 🔧 Setup Instructions
1. **Clone the repository**:
   ```bash
   git clone https://github.com/imannoor22/volume-control-using-hand-gesture.git
   cd volume-control-using-hand-gesture
   ```

2. **Install dependencies**:
   Run the following command to install all the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the program**:
   Simply run the following command to start controlling the volume using hand gestures:
   ```bash
   python volume_control_using_hand_gesture.py
   ```

4. **How It Works**:
   - The program captures video from your webcam.
   - It detects hand landmarks using **MediaPipe**.
   - When the thumb and index finger come closer or move apart, it calculates the distance between them and adjusts the volume accordingly.
   - Visual feedback is provided via the on-screen bar and percentage display.

### ✨ Features in Detail

1. **Hand Tracking**:
   - Uses the **MediaPipe** library to detect hand landmarks and identify the thumb and index finger.

2. **Volume Adjustment**:
   - The distance between the thumb and index finger is calculated using the Euclidean distance formula.
   - This distance is mapped to the system’s volume range using **NumPy's `interp`** function.

3. **Visual Feedback**:
   - The system displays two circles at the thumb and index fingertips and draws a line between them.
   - A dynamic rectangle serves as a visual volume bar that adjusts based on the calculated volume percentage.

### 📂 Project Structure
```
├── career_mentor.py           # Main Python file for volume control
├── README.md                  # Project documentation
└── .gitignore                 # Git ignore file
```

### 📖 Future Enhancements
- Add gesture recognition for **mute/unmute** functionality.
- Improve the accuracy and robustness of hand tracking under different lighting conditions.
- Extend to other system controls like brightness adjustment or media playback.
