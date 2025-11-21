# 🧠 SmartFarm AI Model – YOLO Animal Detector

This directory contains the **YOLO-based object detection model** used in the SmartFarm system to identify common farm-intruding animals in real time.  
The model is optimized for **mobile camera frames** and performs efficiently on CPU-based environments.

---

## 🔍 What the Model Detects

The model is trained/fine-tuned to detect the following intruding animals commonly found in Indian farmlands:

- 🐒 **Monkey**
- 🐐 **Goat**
- 🐄 **Cow**
- 🦌 **Nilgai**
- 🐗 **Wild Boar**

These five classes represent the majority of crop-damaging animal incidents across agricultural regions.

---

## ⚡ How the Model Works

1. The mobile device captures a frame from the live camera feed.  
2. The frame is sent to the backend, which forwards it to the AI model.  
3. The YOLO model performs inference and returns:
   - **Predicted animal label**
   - **Confidence score**
   - **Bounding box** (`x`, `y`, `width`, `height`)
4. The backend uses the results to trigger real-time alerts in the app.

---

## 🚀 Why YOLO?

- ⚡ **Real-time performance**  
- 🎯 **High accuracy** for small & large animal detection  
- 💻 **Runs on CPU** (no GPU required)  
- 🔧 **Easy to retrain** for additional animals  
- 📱 **Optimized for mobile-captured frames**

---

## 📤 Example Model Output (JSON)

```json
{
  "label": "Monkey",
  "confidence": 0.87,
  "box": { "x": 120, "y": 60, "w": 200, "h": 260 }
}
