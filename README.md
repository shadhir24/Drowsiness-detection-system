# 👁️ Drowsiness Detection System

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green)](https://opencv.org/)
[![Keras](https://img.shields.io/badge/Keras-2.x-red)](https://keras.io/)

A real-time drowsiness detection system using computer vision and deep learning to prevent accidents caused by sleepy drivers.


## 🚀 Features

- Real-time eye state detection (open/closed)
- Drowsiness scoring system with adjustable sensitivity
- Visual and audio alerts when drowsiness detected
- Lightweight CNN model for fast inference
- Works with standard webcams
- Customizable alarm sound

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/drowsiness-detection.git
cd drowsiness-detection
```

2. Create and activate virtual environment:
```bash
python -m venv tf_env
source tf_env/bin/activate  # Linux/Mac
.\tf_env\Scripts\activate   # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## 🖥️ Usage

Run the detection system:
```bash
python drowsinessdetection.py
```

Controls:
- Press 'q' to quit
- Adjust `score` threshold in code for sensitivity (default: 15)

## ⚙️ Technical Details

### Model Architecture
- Input: 24x24 grayscale eye images
- 3 Convolutional layers (32, 32, 64 filters)
- Max Pooling and Dropout layers
- Dense layers for classification
- Output: Binary classification (open/closed)

### Detection Logic
- Uses Haar cascades for face and eye detection
- Processes each eye separately through CNN
- Maintains a drowsiness score based on eye states
- Triggers alarm when score exceeds threshold

## 📝 Requirements
- Python 3.8+
- OpenCV
- Keras
- TensorFlow
- Pygame
- Numpy
