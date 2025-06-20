# image_detection
A simple Python project using YOLOv5x and PyTorch to perform real-time object detection on images. 🚀 Detects multiple objects, displays bounding boxes, and saves output — fast, efficient, and beginner-friendly!
# 🦾 YOLOv5 Object Detection using PyTorch

Detect objects in images using the powerful **YOLOv5x** model via PyTorch. This project is simple, effective, and beginner-friendly 💡

---

## 🧠 Model Details

| Model     | Framework | Source                     |
|-----------|-----------|----------------------------|
| YOLOv5x   | PyTorch   | [Ultralytics](https://github.com/ultralytics/yolov5) |

> ⚠️ `yolov5x` is the most accurate model in the YOLOv5 family (but also the largest in size).

---

## 📂 Project Structure

📁 yolov5-object-detection/
├── 📄 detect.py # Main Python script
├── 🖼️ final.jpg # Input image file
├── 📄 README.md # Project description
└── 📄 requirements.txt # Python dependencies (optional)

## 🖥️ Setup Instructions

### ✅ 1. Clone or Download
```bash
git clone https://github.com/your-username/yolov5-object-detection.git
cd yolov5-object-detection

✅ 2. Install Dependencies

pip install torch torchvision matplotlib opencv-python
Or install from requirements.txt:


pip install -r requirements.txt
🚀 Run the Detection
Make sure final.jpg is in the same folder. Then run:


python detect.py
This will:

🔍 Detect objects

🖼️ Show output with bounding boxes

💾 Save result inside: runs/detect/exp/

💡 Sample Output
After running the script, you’ll see console output like:

image 1/1 final.jpg: 2 persons, 1 dog, 1 bicycle
And an image like this gets saved:

🧪 Script Overview

import torch

model = torch.hub.load('ultralytics/yolov5', 'yolov5x', pretrained=True)
model.conf = 0.1

img = 'final.jpg'
results = model(img, size=980)

results.show()
results.save()
results.print()
print(results.pandas().xyxy[0])
🧾 requirements.txt
torch
torchvision
opencv-python
matplotlib
🙋 Author

Madhu Mitha
📍 GitHub: @your-username

🌟 Show Some Love
If you liked this project, give it a ⭐ on GitHub to support!
Made with ❤️ using Python & YOLOv5

