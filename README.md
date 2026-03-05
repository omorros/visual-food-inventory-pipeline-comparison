# VLM vs. YOLO vs. CNN: A Pipeline Comparison for Visual Food Inventory

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.15+-FF6F00?logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.1+-EE4C2C?logo=pytorch&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-Ultralytics-00FFFF?logo=yolo&logoColor=black)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--5.2-412991?logo=openai&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-0.81-61DAFB?logo=react&logoColor=black)
![Expo](https://img.shields.io/badge/Expo_SDK-54-000020?logo=expo&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=typescript&logoColor=white)

BSc (Hons) Software Engineering — Anglia Ruskin University
Final Year Dissertation | Supervisor: Dr Vitaliy Milke

Comparing three computer vision pipelines for automated food item
recognition from fridge/shelf images, evaluated across degraded
imaging conditions on a 14-class dataset.

## Experiments

| # | Repository | Description |
|---|-----------|-------------|
| 1 | [food-cv-exp1-cnn-comparison](https://github.com/omorros/food-cv-exp1-cnn-comparison) | Benchmarks EfficientNetB0, ResNet-50 and a custom CNN on 120k food images to select the best classifier for downstream pipelines |
| 2 | [food-cv-exp2-pipeline-evaluation](https://github.com/omorros/food-cv-exp2-pipeline-evaluation) | Compares a VLM, YOLOv8 and YOLOv8+EfficientNetB0 pipeline across 4 image conditions on 120 test images to find the most accurate and robust approach |
| 3 | [food-cv-exp3-mobile-deployment](https://github.com/omorros/food-cv-exp3-mobile-deployment) | Deploys the winning GPT-5.2 Vision pipeline into a full stack React Native + FastAPI app with draft review, inventory management and expiry prediction |

## Tech Stack

### Experiment 1 — CNN Classifier Selection
| Category | Tools |
|----------|-------|
| ML Framework | TensorFlow / Keras |
| Models | EfficientNetB0, ResNet-50, Custom CNN (ImageNet pretrained) |
| Data & Evaluation | NumPy, Pandas, scikit-learn |
| Visualization | Matplotlib |
| Environment | Google Colab (Tesla T4 GPU) |

### Experiment 2 — Pipeline Evaluation
| Category | Tools |
|----------|-------|
| Object Detection | YOLOv8 (Ultralytics 8.3.57) |
| VLM APIs | OpenAI GPT-5.2, Anthropic Claude Opus 4.6, Google Gemini 3.1 Pro |
| CNN Classifier | TensorFlow / Keras (EfficientNetB0) |
| Deep Learning | PyTorch + TorchVision |
| Image Processing | Pillow, OpenCV |
| Data & Evaluation | NumPy, Pandas, scikit-learn, Seaborn, Matplotlib |
| Dataset Source | Roboflow Universe (42k images, 47 classes) |
| Utilities | python-dotenv, Rich, structlog, PyYAML |
| Environment | Google Colab (Tesla T4 GPU) |

### Experiment 3 — Mobile Deployment (SnapShelf)
| Category | Tools |
|----------|-------|
| Mobile | React Native 0.81, Expo SDK 54, TypeScript 5.9 |
| Navigation & UI | Expo Router, Expo Haptics, Expo Linear Gradient, Ionicons |
| Camera & Storage | Expo Image Picker, Expo Camera, Expo Secure Store |
| Gestures | react-native-gesture-handler |
| Backend | FastAPI, SQLAlchemy, Uvicorn |
| Database | PostgreSQL (psycopg2) |
| Auth | JWT (python-jose), bcrypt / passlib |
| Vision API | OpenAI GPT-5.2 Vision |
| Validation | Pydantic, email-validator |

## Key Findings

- VLM pipeline achieved F1 = 0.900 vs YOLO-14's F1 = 0.603
- VLM demonstrated significantly greater robustness to image degradation
- EfficientNetB0 selected as best CNN classifier (statistically equivalent to ResNet-50 at ~5× smaller size)