<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=DeepFake%20Detection&fontSize=46&fontColor=00d9ff&fontAlignY=38&desc=ResNext%20CNN%20%2B%20LSTM%20%7C%20Transfer%20Learning%20%7C%20Django&descAlignY=58&descSize=16&descColor=a78bfa" />

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=20&pause=1000&color=00D9FF&center=true&vCenter=true&width=750&lines=Detecting+manipulated+media+with+AI+%F0%9F%94%8D;ResNext+CNN+%2B+LSTM+Hybrid+Pipeline+%F0%9F%A7%A0;93.59%25+Accuracy+on+6%2C000+Videos+%F0%9F%8F%86;Real-time+Detection+via+Django+Web+App+%F0%9F%9A%80" alt="Typing SVG" />

<br/><br/>

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org)
[![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)](https://djangoproject.com)
[![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org)

[![GitHub stars](https://img.shields.io/github/stars/arryansharma1/Deep-Fake-Detection?style=for-the-badge&color=f59e0b&labelColor=0d1117&logo=github)](https://github.com/arryansharma1/Deep-Fake-Detection/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/arryansharma1/Deep-Fake-Detection?style=for-the-badge&color=00d9ff&labelColor=0d1117&logo=github)](https://github.com/arryansharma1/Deep-Fake-Detection/network)
[![License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge&labelColor=0d1117)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/arryansharma1/Deep-Fake-Detection?color=7c3aed&labelColor=0d1117&style=for-the-badge)](https://github.com/arryansharma1/Deep-Fake-Detection)

<br/>

> ### *"In a world where seeing is no longer believing — AI fights back."*

<br/>

[📖 Documentation](https://github.com/arryansharma1/Deep-Fake-Detection/tree/main/Documentation) &nbsp;•&nbsp; [🐛 Report Bug](https://github.com/arryansharma1/Deep-Fake-Detection/issues) &nbsp;•&nbsp; [💡 Request Feature](https://github.com/arryansharma1/Deep-Fake-Detection/issues)

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

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

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 🧠 Introduction

<img align="right" width="280" src="https://media.giphy.com/media/3o6MbbwX2g2GA4MUus/giphy.gif"/>

Deepfake videos pose a serious threat to media integrity, leveraging AI to convincingly swap faces or manipulate content. This project presents a **hybrid deep learning pipeline** to accurately detect deepfake videos using:

- 🔷 **ResNext CNN** — A powerful convolutional architecture for per-frame **spatial feature extraction** via transfer learning
- 🔷 **LSTM Network** — Captures **temporal dependencies** across video frames to learn manipulation patterns over time

The model achieves up to **93.59% accuracy**, trained on a curated dataset of **6,000 real and fake videos**.

> 📄 Detailed methodology and findings are available in the [Documentation folder](https://github.com/arryansharma1/Deep-Fake-Detection/tree/main/Documentation).

<br clear="right"/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 🏗️ System Architecture

<div align="center">

<img src="https://github.com/abhijitjadhav1998/Deepfake_detection_using_deep_learning/blob/master/github_assets/System%20Architecture.png" width="80%"/>

</div>

<br/>

**Pipeline Overview:**

```
Video Input ──► Frame Extraction ──► ResNext (Feature Vectors) ──► LSTM ──► Real / Fake
```

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 🎬 Demo

<div align="center">

<img src="https://github.com/abhijitjadhav1998/Deepfake_detection_using_deep_learning/blob/master/github_assets/fakegif.gif" width="80%"/>

*Real-time deepfake detection using ResNext + LSTM hybrid model*

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 📊 Results

<div align="center">

| Model | Videos | Frames Sampled | Accuracy | Status |
|:---:|:---:|:---:|:---:|:---:|
| `model_89_acc_40_frames_final_data.pt` | 6,000 | 40 | **89.35%** | ☑️ Tested |
| `model_93_acc_100_frames_final_data.pt` | 6,000 | 100 | **93.59%** | ✅ Best |

</div>

<br/>

> 🏆 The **100-frame model** achieves our best accuracy of **93.59%**, leveraging richer temporal context per prediction — more frames means the LSTM sees more manipulation artifacts over time.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 📂 Directory Structure

```
📦 Deepfake_Detection_Using_Deep_Learning/
│
├── 📁 Django_Application/
│   ├── Frontend UI (Video Upload)
│   ├── Backend Model Integration
│   └── Result Display
│
├── 📁 Model_Creation/
│   ├── Data Preprocessing
│   ├── Feature Extraction (ResNext)
│   ├── LSTM Training
│   └── Model Evaluation
│
└── 📁 Documentation/
    ├── Project Reports
    ├── Technical Insights
    └── Research References
```

| 📁 Folder | 📋 Description |
|:---|:---|
| 🖥️ `Django_Application` | Web interface for uploading videos and displaying detection results in real-time |
| 🧪 `Model_Creation` | End-to-end pipeline: dataset prep, ResNext feature extraction, LSTM training & evaluation |
| 📚 `Documentation` | Research reports, technical architecture notes, and academic references |

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## ⚡ Installation & Setup

### Prerequisites

![Python](https://img.shields.io/badge/Python_3.8+-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Pillow](https://img.shields.io/badge/Pillow-3776AB?style=flat-square&logo=python&logoColor=white)

### Steps

```bash
# 📥 Clone the repository
git clone https://github.com/arryansharma1/Deep-Fake-Detection.git
cd Deep-Fake-Detection

# 📦 Install dependencies
pip install -r requirements.txt

# 🚀 Launch the Django application
cd Django_Application
python manage.py runserver
```

Then open your browser at `http://127.0.0.1:8000/` and upload a video to test detection.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 🔍 How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│  1. VIDEO INGESTION   →   Upload .mp4 / .avi via web interface  │
│           │                                                     │
│           ▼                                                     │
│  2. FRAME EXTRACTION  →   Sample N frames uniformly from video  │
│           │                                                     │
│           ▼                                                     │
│  3. FEATURE EXTRACT   →   ResNext CNN → 2048-dim vector/frame   │
│           │                                                     │
│           ▼                                                     │
│  4. TEMPORAL MODEL    →   LSTM learns manipulation over time    │
│           │                                                     │
│           ▼                                                     │
│  5. CLASSIFICATION    →   Sigmoid → REAL or FAKE + confidence   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 🤝 Contributing

Contributions are warmly welcome! Here's how you can help:

```bash
# 1. Fork the repository & create your branch
git checkout -b feature/YourFeature

# 2. Commit your changes
git commit -m "Add YourFeature"

# 3. Push and open a Pull Request
git push origin feature/YourFeature
```

Please ensure your code follows the existing structure and includes appropriate documentation.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 👤 Author

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-arryansharma1-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/arryansharma1)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-arryansharma-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/arryansharma/)
[![Email](https://img.shields.io/badge/Email-aryansharma7341.as@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:aryansharma7341.as@gmail.com)

</div>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=120&section=footer&text=Thanks+for+visiting!+%F0%9F%A4%96&fontSize=24&fontColor=00d9ff&fontAlignY=65"/>

<br/>

⭐ **If this project was helpful, please consider giving it a star — it means a lot!**

*Made with ❤️ and deep learning*

![Visitor Count](https://komarev.com/ghpvc/?username=arryansharma1&color=00d9ff&style=for-the-badge&label=PROFILE+VIEWS)

</div>
