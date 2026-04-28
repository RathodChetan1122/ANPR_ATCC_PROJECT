# 🚗 Smart Traffic Monitoring System — ANPR / ATCC

> Real-time Automatic Number Plate Recognition (ANPR) and Automatic Traffic Classification & Counting (ATCC) using Computer Vision and Flask REST APIs.

---

## 📌 Overview

A computer vision–based traffic monitoring application that detects and classifies vehicles from live video streams, recognizes number plates with **~92% accuracy**, and processes footage at **~25 FPS**. Detection results are served via REST APIs and stored in a structured MySQL database for reporting and analysis.

Built as part of the **Infosys Internship Program**.

---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| Computer Vision | Python, OpenCV, YOLOv |
| Backend / API | Flask, REST API |
| Database | MySQL |
| Architecture | OOP, Modular Pipeline |
| Notebook | Jupyter Notebook |

---

## ✨ Features

- 🔍 **ANPR** — Detects and reads vehicle number plates from live/recorded video
- 🚦 **ATCC** — Classifies and counts vehicles by type (car, truck, bike, etc.)
- ⚡ **Real-time processing** — ~25 FPS with optimized OpenCV preprocessing
- 📡 **REST API** — Flask endpoints to serve detection results to client apps
- 🗄️ **MySQL storage** — Stores classified vehicle data with structured schema
- 📊 **Audit logging** — Tracks detection events for reporting

---

## 🗂️ Project Structure

```
ANPR_ATCC_PROJECT/
│
├── ATCC_Infosys_Internship/
│   ├── anpr_detection.ipynb       # Number plate recognition pipeline
│   ├── atcc_classification.ipynb  # Vehicle classification & counting
│   ├── app.py                     # Flask REST API server
│   ├── models/                    # Trained model files
│   ├── utils/                     # OOP helper modules
│   └── database/                  # MySQL schema & queries
│
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

```bash
Python 3.8+
MySQL 8.0+
```

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/RathodChetan1122/ANPR_ATCC_PROJECT.git
cd ANPR_ATCC_PROJECT

# 2. Install dependencies
pip install -r requirements.txt

# 3. Set up the database
mysql -u root -p < database/schema.sql

# 4. Run the Flask server
python app.py
```

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/detections` | Fetch all detection records |
| `POST` | `/api/detect` | Submit a video frame for detection |
| `GET` | `/api/vehicles` | Get classified vehicle summary |

---

## 📊 Performance

| Metric | Result |
|---|---|
| Number Plate Recognition Accuracy | ~92% |
| Processing Speed | ~25 FPS |
| Dataset | Live video stream + test footage |

---

## 🧠 How It Works

```
Video Stream → OpenCV Preprocessing → YOLO Detection
     → Number Plate Extraction → OCR Recognition
          → Flask API → MySQL Storage → Client Dashboard
```

---

## 📄 License

This project was developed as part of an internship program. For educational and demonstration purposes only.

---

## 👤 Author

**Chetan Rathod**
[GitHub](https://github.com/RathodChetan1122)
