# ✋🤖 Sign Language Detection Using YOLOv5

This project implements a real-time **Sign Language Recognition System** using **YOLOv5**, a powerful object detection model developed by Ultralytics. The system is trained to recognize key American Sign Language (ASL) gestures and display their corresponding labels.

---

## 📽️ Demo

> 🎥 A webcam window displays bounding boxes and labels as you perform signs in front of your camera.

---

## 📂 Project Structure

ign-Language-Detection-YOLOv5/
│
├── yolov5/ # YOLOv5 model and scripts
├── Data/ # Optional: contains datasets and test images
├── env/ # Virtual environment (should be excluded)
├── best.pt # Trained YOLOv5 model (not uploaded to GitHub)
├── run.py # Script to launch webcam-based detection
├── capture_image.py # (Optional) tool to collect training data
├── data.yaml # Defines dataset classes
├── test_webcam.py # Script to test your webcam
└── README.md # This file

yaml
Copy code

---

## 🧠 Classes Trained

```yaml
names:
  - Hello
  - IloveYou
  - No
  - Please
  - Thanks
  - Yes
🚀 How to Run
Clone the repo:

bash
Copy code
git clone https://github.com/your-username/sign-language-detection-yolov5.git
cd sign-language-detection-yolov5
Install dependencies (use Conda or pip):

bash
Copy code
pip install -r yolov5/requirements.txt
pip install opencv-python numpy
Activate your environment and run:

bash
Copy code
python run.py
Make sure best.pt is in the correct location (yolov5/best.pt or change path in run.py).

🧪 Test on Images
bash
Copy code
python yolov5/detect.py --weights yolov5/best.pt --img 416 --source Data/images/sample.jpg --view-img
✍️ Model Training (if needed)
Use train.py in YOLOv5:

bash
Copy code
python yolov5/train.py --img 416 --batch 16 --epochs 50 --data data.yaml --weights yolov5s.pt --project runs/train


