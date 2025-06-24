# Player Re-Identification in Sports Footage

This project performs player detection and re-identification in a football match video using the YOLO object detection model and the Deep SORT tracking algorithm. It processes a short video clip and outputs a new video where each player is tracked and consistently labeled throughout the footage.

---

## 📚 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)

---

## 🧠 Overview

The project takes a video of a football match (`football.mp4`) and applies the following pipeline:

1. **YOLOv8** is used to detect all objects in each frame.
2. Only football players are retained (excluding class ID 0, which is often "person").
3. **Deep SORT** assigns consistent IDs to players across frames using both motion and appearance features.
4. The final output video (`out.mp4`) shows each detected player in a unique color with a label (e.g., `Player 3`).

---

## ✨ Features

- Detects and tracks football players in video footage
- Maintains player identities across frames
- Annotates output video with colored bounding boxes and player labels
- Modular structure with YOLO detection and Deep SORT tracking components

---

## 🛠 Technologies Used

- **YOLO (Ultralytics)** – Object detection
- **Deep SORT** – Player re-identification and multi-object tracking
- **OpenCV** – Video processing and visualization
- **TensorFlow** – For Deep SORT's appearance feature encoder
- **NumPy** – Array manipulations

---

## ⚙️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/player-reid-footage.git
   cd player-reid-footage
