# 🛒 Retail Surveillance Pedestrian Tracking  
*A YOLOv8 + Multi-Object Tracking (MOT) System for Persistent Person Tracking in Retail Environments*  

---

## 📌 Overview  
This project was developed for the **Fawry AI/ML Competition**, focusing on **retail surveillance and pedestrian tracking**.  
The goal is to **detect and track individuals in crowded retail environments** while assigning **persistent unique IDs** to each person across frames.  

We built a **robust person tracking pipeline** using **YOLOv8 fine-tuned for detection** combined with multiple **state-of-the-art MOT trackers**.  
Our final system achieved a **MOTA (Multiple Object Tracking Accuracy) score of 77**, ensuring reliable tracking in complex retail settings.  

---

## 🧩 Key Features  
- **YOLOv8 Fine-tuned Detector** → trained on **28k+ annotated retail pedestrian images**.  
- **Custom Data Collection & Annotation** → combined data from multiple sources, merged with unique renaming, and annotated using **RoboFlow**.  
- **Multi-Tracker Experiments**:  
  - **ByteTrack**  
  - **BoT-SORT**  
  - **DeepSORT**  
- **Re-ID Models Integration**: tested **FastReID** and other re-identification modules for consistent ID assignment.  
- **Tracker Parameter Fine-Tuning** → optimized hyperparameters and re-ID thresholds for higher robustness in crowded retail stores.  
- **High MOTA (77%) Performance** → reliable tracking with low ID switches.  

---

## ⚙️ Methodology  

### 1. Data Preparation  
- Collected diverse datasets (surveillance, retail, open pedestrian datasets).  
- Merged them into a **28k-image dataset**.  
- Ensured **file uniqueness** through systematic renaming.  
- Manually refined **bounding box annotations** using **RoboFlow** for accuracy.  

### 2. Detection Model – YOLOv8  
- Started with pretrained YOLOv8 weights.  
- Fine-tuned on **28k annotated images**.  
- Achieved strong person detection accuracy even in **occluded & crowded environments**.  

### 3. Tracking Models  
We experimented with different **MOT algorithms**:  
- **ByteTrack** → fast & accurate baseline.  
- **BoT-SORT** → stronger handling of occlusion cases.  
- **DeepSORT** → combined with **ReID models** for persistent ID assignment.  

#### Re-ID Integration  
- Integrated **FastReID** and tuned embedding thresholds.  
- Reduced **ID switches** significantly in crowded frames.  

### 4. Tracker Optimization  
- Adjusted tracking hyperparameters: confidence thresholds, max_age, iou_distance.  
- Tuned ReID embeddings for **optimal identity preservation**.  

---

## 📊 Results  
- **MOTA Score**: **77%**  
- **High ID Consistency**: persistent unique IDs across sequences.  
- **Scalability**: effective for retail surveillance, crowd monitoring, and anomaly detection use cases.  

---

## 🚀 Applications  
- Retail analytics → customer flow monitoring, heatmap generation.  
- Security surveillance → detect suspicious behavior, loitering.  
- Smart stores → anonymous tracking of shoppers for better service optimization.  

---

## 🏆 Competition Achievement  
This project was submitted to the **Fawry AI/ML Competition** as a **Retail Surveillance Pedestrian Tracking solution**, showcasing:  
- **Strong MOT20 benchmark adaptation**  
- **Real-world applicability in retail settings**  
- **Optimized YOLOv8 + MOT pipeline with high MOTA performance**  

---

## 📌 Tech Stack  
- **YOLOv8** – Person Detection  
- **ByteTrack / BoT-SORT / DeepSORT** – Tracking  
- **FastReID** – Re-identification  
- **RoboFlow** – Annotation Tool  
- **PyTorch / Ultralytics** – Training & Inference  
