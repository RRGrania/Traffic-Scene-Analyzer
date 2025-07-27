# 🛣️ Traffic Scene Analysis with Vision and Language Models

This project combines computer vision and multimodal language models to analyze traffic scenes. It performs three main tasks:

1. **Traffic Scene Description** – Uses a Vision-Language Model (VLM) to generate a textual description of the traffic image.
2. **License Plate Detection & OCR** – Detects license plates using YOLOv8 and extracts plate numbers using OCR.
3. **Counting Vehicles and Plates** – Counts the number of cars and license plates present in the image.

---

## 🔧 Pipeline Overview

The pipeline consists of the following key steps:

1. **Input Image Upload**: User uploads a traffic scene image through the Gradio interface.
2. **Scene Description**:
   - A Vision-Language Model (e.g., Qwen-VL or similar) processes the image and generates a natural language description.
3. **License Plate Detection**:
   - YOLOv8 is used to detect bounding boxes around license plates.
4. **OCR Extraction**:
   - Extracted regions are processed using **EasyOCR** or optionally **PaddleOCR** to read license plate numbers.
5. **Counting**:
   - The number of license plates and detected cars are counted.
6. **Output**:
   - The Gradio interface displays the annotated image, detected license plate numbers, and generated text description.

---

## 📁 Code Structure

- `traffic_scene.ipynb`: Full notebook with all code (YOLO detection, VLM description, OCR, Gradio UI).
- `README.md`: Project documentation.

---

## 📦 Installation Requirements

To run the project, install the following dependencies:

```bash
pip install -q gradio>=4.0.0
pip install -q ultralytics>=8.0.0
pip install -q transformers>=4.30.0
pip install -q accelerate>=0.20.0
pip install -q torch torchvision torchaudio
pip install -q pillow opencv-python-headless
pip install -q numpy>=1.21.0
pip install -q easyocr
