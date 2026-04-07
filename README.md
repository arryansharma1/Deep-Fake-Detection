<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1a1f2e,100:0f3460&height=200&section=header&text=DeepFake%20Detection&fontSize=50&fontColor=00d4ff&fontAlignY=38&desc=ResNext%20%2B%20LSTM%20%7C%20Deep%20Learning&descAlignY=60&descSize=18&descColor=8b949e" alt="banner"/>

<br/>

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org)
[![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)](https://djangoproject.com)
[![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org)

[![GitHub stars](https://img.shields.io/github/stars/arryansharma1/Deep-Fake-Detection?style=for-the-badge&color=FFD700&logo=github)](https://github.com/arryansharma1/Deep-Fake-Detection/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/arryansharma1/Deep-Fake-Detection?style=for-the-badge&color=00d4ff&logo=github)](https://github.com/arryansharma1/Deep-Fake-Detection/network)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

<br/>

> **Detecting manipulated media with 93.59% accuracy using transfer learning — ResNext CNN + LSTM**

<br/>

[📖 Documentation](https://github.com/arryansharma1/Deep-Fake-Detection/tree/main/Documentation) &nbsp;•&nbsp; [🐛 Report Bug](https://github.com/arryansharma1/Deep-Fake-Detection/issues) &nbsp;•&nbsp; [💡 Request Feature](https://github.com/arryansharma1/Deep-Fake-Detection/issues)

</div>

---

## 📌 Table of Contents

- [Introduction](#-introduction)
- [System Architecture](#-system-architecture)
- [Demo](#-demo)
- [Results](#-results)
- [Directory Structure](#-directory-structure)
- [Installation & Setup](#-installation--setup)
- [How It Works](#-how-it-works)
- [Contributing](#-contributing)
- [Author](#-author)

---

## 🧠 Introduction

Deepfake videos pose a serious threat to media integrity, leveraging AI to convincingly swap faces or manipulate content. This project presents a **hybrid deep learning pipeline** to accurately detect deepfake videos using:

- 🔷 **ResNext CNN** — A powerful convolutional architecture used for per-frame **spatial feature extraction** via transfer learning.
- 🔷 **LSTM Network** — Captures **temporal dependencies** across video frames to learn manipulation patterns over time.

The model achieves up to **93.59% accuracy**, trained on a curated dataset of 6,000 real and fake videos.

> 📄 Detailed methodology and findings are available in the [Documentation folder](https://github.com/arryansharma1/Deep-Fake-Detection/tree/main/Documentation).

---

## 🏗️ System Architecture

<p align="center">
  <img src="https://github.com/abhijitjadhav1998/Deepfake_detection_using_deep_learning/blob/master/github_assets/System%20Architecture.png" alt="System Architecture" width="80%"/>
</p>

**Pipeline overview:**

```
Video Input ──► Frame Extraction ──► ResNext (Feature Vectors) ──► LSTM ──► Real / Fake
```

---

## 🎬 Demo

<p align="center">
  <img src="https://github.com/abhijitjadhav1998/Deepfake_detection_using_deep_learning/blob/master/github_assets/fakegif.gif" alt="Deepfake Detection Demo" width="80%"/>
</p>

---

## 📊 Results

| Model | Videos | Frames | Accuracy |
|:------|:------:|:------:|:--------:|
| `model_89_acc_40_frames_final_data.pt` | 6,000 | 40 | **89.35%** |
| `model_93_acc_100_frames_final_data.pt` | 6,000 | 100 | **93.59%** ✅ |

> 🏆 The **100-frame model** achieves our best accuracy of **93.59%**, leveraging richer temporal context per prediction.

---

## 📂 Directory Structure

```
Deepfake_Detection_Using_Deep_Learning/
│
├── 🖥️  Django_Application/
│   ├── Frontend UI (Video Upload)
│   ├── Backend Model Integration
│   └── Result Display
│
├── 🧪  Model_Creation/
│   ├── Data Preprocessing
│   ├── Feature Extraction (ResNext)
│   ├── LSTM Training
│   └── Model Evaluation
│
└── 📚  Documentation/
    ├── Project Reports
    ├── Technical Insights
    └── Research References
```

| Folder | Description |
|:-------|:------------|
| `Django_Application` | Web interface for uploading videos and displaying deepfake detection results in real-time. |
| `Model_Creation` | End-to-end pipeline: dataset prep, ResNext feature extraction, LSTM training, and evaluation scripts. |
| `Documentation` | Research reports, technical architecture notes, and academic references. |

---

## ⚡ Installation & Setup

### Prerequisites

Ensure the following are installed on your system:

- Python `3.8+`
- pip

### Quickstart

```bash
# 1. Clone the repository
git clone https://github.com/arryansharma1/Deep-Fake-Detection.git
cd Deep-Fake-Detection

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the Django application
cd Django_Application
python manage.py runserver
```

Then open your browser at `http://127.0.0.1:8000/` and upload a video to test detection.

### Dependencies

```txt
torch
torchvision
django
opencv-python
numpy
pillow
```

---

## 🔍 How It Works

```
1. VIDEO INGESTION     Upload a .mp4 / .avi file via the web interface
        │
        ▼
2. FRAME EXTRACTION    Sample N frames uniformly from the video
        │
        ▼
3. FEATURE EXTRACTION  Feed each frame through pre-trained ResNext CNN
                       → Output: 2048-dim feature vector per frame
        │
        ▼
4. TEMPORAL MODELING   Sequence of vectors passed through LSTM
                       → Learns manipulation patterns over time
        │
        ▼
5. CLASSIFICATION      Sigmoid output → REAL or FAKE + confidence score
```

---

## 🤝 Contributing

Contributions are warmly welcome! Here's how you can help:

1. **Fork** the repository
2. Create a feature branch: `git checkout -b feature/YourFeature`
3. Commit your changes: `git commit -m 'Add YourFeature'`
4. Push to the branch: `git push origin feature/YourFeature`
5. Open a **Pull Request**

Please ensure your code follows the existing structure and includes appropriate documentation.

---

## 👤 Author

<div align="left">

[![GitHub](https://img.shields.io/badge/GitHub-arryansharma1-181717?style=for-the-badge&logo=github)](https://github.com/arryansharma1)<br /><br />
[![LinkedIn](https://img.shields.io/badge/LinkedIn-arryansharma-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/arryansharma/)<br /><br />
[![Email](https://img.shields.io/badge/Email-aryansharma7341.as%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:aryansharma7341.as@gmail.com)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f3460,50:1a1f2e,100:0d1117&height=100&section=footer" alt="footer"/>

**⭐ If this project was helpful, please consider giving it a star — it means a lot!**

*Made with ❤️ and deep learning*

</div>
