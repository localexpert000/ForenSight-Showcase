# 🧠 Verified AI Capabilities

ForenSight AI implements the following detection modules, verified in our production codebase.

---

## 1. Human Analytics
*   **Face Recognition:** Identifies registered individuals using ArcFace (ResNet100) embeddings.
*   **Person Detection:** High-accuracy human detection using YOLOv8 optimized for checking "Human" class.
*   **Face Detection:** Specialized YOLOv5-Face model for detecting faces in difficult lighting/angles.
*   **Person Re-Identification (ReID):** Tracks a specific person across multiple cameras by appearance.
*   **Crowd Counting:** Real-time estimation of crowd density in a specific ROI.
*   **Uniform Detection:** Identifies staff members based on HSV color analysis of upper-body clothing.

## 2. Security & Forensics
*   **Weapon Detection:** Specialized model trained to detect Handguns, Rifles, and Knives with high priority alerting.
*   **Fire & Smoke Detection:** Visual detection of flames and smoke plumes for early warning.
*   **Fighting/Violence Detection:** Action recognition model detecting aggressive physical interactions.
*   **Intrusion Detection:** "Virtual Tripwire" logic to detect unauthorized entry into drawn zones.
*   **Theft Detection:** Asset protection module monitoring specific objects for removal.
*   **Abandoned Object:** Detects bags/luggage left unattended for >30 seconds.

## 3. Vehicle Analytics
*   **License Plate Recognition (ALPR):** Captures and OCRs license plates for access control logs.
*   **Vehicle Classification:** Distinguishes between Car, Truck, Bus, Motorbike.
*   **Vehicle Color Recognition:** K-Means clustering to identify "Red Car", "White Van", etc.
*   **Illegal Parking:** Detects vehicles stationary in "No Parking" zones.
*   **Wrong-Way Detection:** Analyzing optical flow vectors against permitted direction.

## 4. Behavioral Analysis
*   **Loitering Detection:** Flags individuals staying in a zone longer than a defined threshold.
*   **Running/Panic Detection:** Velocity analysis of skeletal keypoints to detect emergency running.
*   **Gait Analysis:** (Experimental) Analyzing walking patterns.
