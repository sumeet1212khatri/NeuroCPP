# NeuroCPP 🧠
> A Neural Network framework built from scratch in C++ — no ML libraries used.

![C++](https://img.shields.io/badge/C++-17-blue?logo=cplusplus)
![Python](https://img.shields.io/badge/Python-3.10-yellow?logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-0.100-green?logo=fastapi)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 About

NeuroCPP is a fully custom Neural Network framework written in **C++ using only the standard library**.
It replicates core PyTorch functionality — forward pass, backpropagation, gradient descent — completely from scratch.
The trained model is served via a **FastAPI REST API** with a **frontend UI** for real-time image classification.

---

## 🎯 Results

| Dataset        | Accuracy |
|----------------|----------|
| MNIST          | 94.6%    |
| Fashion MNIST  | 83.8%    |

> Fully replicates PyTorch baseline — without using any ML library.

---

## 🏗️ Architecture

```
Frontend (HTML/JS)
      ↓  image upload
FastAPI (Python)
      ↓  subprocess call
C++ Compiled Binary
      ↓  inference
Prediction + Confidence %
```

---

## ✅ Features

- Neural Network built in **pure C++** (no PyTorch, TensorFlow, or Sklearn)
- Manually implemented:
  - Forward Pass
  - Backpropagation
  - ReLU & Softmax Activation
  - Cross-Entropy Loss
  - Stochastic Gradient Descent (SGD)
  - Matrix Multiplication
- FastAPI backend for REST API
- Frontend UI — drag & drop image upload
- Dockerized for easy deployment

---

## 📁 Project Structure

```
NeuroCPP/
├── cpp/
│   ├── main.cpp          # Entry point
│   ├── neural_net.cpp    # Core NN framework
│   ├── matrix.cpp        # Matrix operations
│   └── CMakeLists.txt    # Build config
├── api/
│   ├── main.py           # FastAPI server
│   └── requirements.txt
├── frontend/
│   ├── index.html
│   └── style.css
├── models/
│   └── weights.bin       # Saved model weights
├── Dockerfile
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/NeuroCPP.git
cd NeuroCPP
```

### 2. Build C++ binary
```bash
cd cpp
mkdir build && cd build
cmake ..
make
```

### 3. Run FastAPI server
```bash
cd api
pip install -r requirements.txt
uvicorn main:app --reload
```

### 4. Open Frontend
```
Open frontend/index.html in your browser
```

---

## 🐳 Docker Deploy

```bash
docker build -t neurocpp .
docker run -p 8000:8000 neurocpp
```

---

## 🛠️ Tech Stack

| Layer     | Technology          |
|-----------|---------------------|
| ML Core   | C++ (standard lib)  |
| Backend   | Python + FastAPI    |
| Frontend  | HTML + CSS + JS     |
| Deploy    | Docker + Railway    |

---

## 📄 License

MIT License — feel free to use and modify.

---

## 🙋 Author

**Your Name**
[GitHub](https://github.com/yourusername) • [LinkedIn](https://linkedin.com/in/yourprofile)
