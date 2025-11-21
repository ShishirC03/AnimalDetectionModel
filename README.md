🧠 AI Model Description (YOLO Animal Detector)

SmartFarm uses a YOLO-based object detection model to identify common farm-intruding animals in real time. The model is optimized for mobile camera frames sent to the backend.

🔍 What the Model Detects

The model is trained/fine-tuned to detect these animals:

Monkey

Goat

Cow

Nilgai

Wild Boar

These reflect the most frequent intruders in Indian farmlands.

⚡ How It Works

Mobile app captures a frame

Frame is sent to the Node.js backend

Backend forwards the image to the YOLO AI model server (FastAPI)

Model returns:

animal label

confidence score

bounding box

Backend saves the detection and sends a real-time alert to the app via Socket.IO

🚀 Why YOLO?

Very fast (real-time inference)

Accurate on small + large animals

Lightweight enough to run on CPU

Easy to retrain for custom animals

📦 Output Example
{
  "label": "Monkey",
  "confidence": 0.87,
  "box": { "x": 120, "y": 60, "w": 200, "h": 260 }
}

🎯 Purpose

To instantly detect dangerous or crop-damaging animals and notify farmers through the app’s alert system.
