# Weapons Detection and Alert System

A real-time AI-powered surveillance system using **YOLO v11** to detect high-alert weapons such as guns, knives, and explosives, with integrated audio alerts to support rapid threat response.

---

##  Overview

This project leverages deep learning and computer vision to automatically detect weapons from images or video streams. By using a custom-trained YOLO model, it identifies threats and triggers specific alert sounds for each detected weapon, aiding rapid and accurate security response.

---

## Key Features

- Real-time object detection using **YOLO v11**
- Identification of high-alert threats: **guns**, **knives**, **explosives**
- Custom audio alerts per detected object
- Robust performance across diverse lighting and background conditions
- Achieved **86.9% mAP** on validation set

---

## Tech Stack

- **Python**
- **YOLO v11 (Ultralytics)**
- **OpenCV** (`cv2`) – image/video processing
- **pygame** – for alert sound playback
- **Roboflow** – dataset preparation and annotation

---

## Implementation

1. **Dataset Collection & Preparation**  
   - Sourced from Roboflow Universe (annotated images of weapons)  
   - Augmented and resized for robust training

2. **Model Training**  
   - YOLO v11 model trained using Ultralytics framework  
   - Used custom configuration with early stopping and learning rate scheduling

3. **Real-Time Detection**  
   - `best.pt` model loaded in a Jupyter notebook  
   - Captures images or streams, performs inference using YOLO  
   - Labels threats as "Gun", "Knife", or "Explosive" in real time

4. **Alert System Integration**  
   - Used `pygame.mixer` to play distinct audio alerts per weapon  
   - Alerts triggered immediately after detection

5. **Visualization**  
   - Bounding boxes with class labels rendered using `cv2.imshow()`  
   - Real-time window displays detected threats

---

## Future Enhancements

- Integrate with **CCTV or drone surveillance feeds**  
- **Deploy on edge devices** (e.g., Jetson Nano, Raspberry Pi)  
- Expand dataset to include **mid-alert tools**  
- Build a **web dashboard** for centralized monitoring

---

## License

Open-source under the **MIT License**. Free to use and modify for academic or research purposes.

