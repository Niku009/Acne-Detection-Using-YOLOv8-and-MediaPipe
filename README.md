# 🧴 Acne Detection Using YOLOv8 and MediaPipe

This project is a smart, deep-learning-powered solution that detects **acne in specific facial regions** using a custom-trained YOLOv8 model. It combines **facial landmark detection** via MediaPipe with **object detection** via YOLOv8 to provide a region-wise analysis — such as acne on the **cheeks**, **forehead**, or **under the eyes** — instead of just binary classification.

---

## 🧠 What It Does

✅ Automatically detects acne on a person's face image  
✅ Divides the face into regions:
- Left Cheek
- Right Cheek
- Forehead
- Under Eyes  
✅ Uses **MediaPipe Face Mesh** to extract facial landmarks and regions  
✅ Uses a **YOLOv8 model** trained on real acne images to detect acne spots  
✅ Classifies acne severity as:
- `Clear`
- `Mild`
- `Moderate`
- `Severe`  
✅ Visualizes detection results using bounding boxes and confidence scores  

---

## 🔧 Tech Stack

| Tool/Library     | Purpose                                 |
|------------------|------------------------------------------|
| 🟣 YOLOv8         | Object detection (Ultralytics v8.2.67)   |
| 🟢 MediaPipe      | Facial landmark detection                |
| 🖼️ OpenCV         | Image reading and preprocessing          |
| 📊 wandb.ai       | Model training tracking and visualization |
| 📈 Matplotlib     | Display detection results                |
| 💻 Google Colab   | Environment used for training & testing  |

---

## 📚 Dataset Used

**Kaggle Dataset**: Acne Detection Dataset in YOLOv8 Format  
📎 [View Dataset on Kaggle](https://www.kaggle.com/datasets/osmankagankurnaz/acne-dataset-in-yolov8-format)

This dataset contains labeled images of faces with acne annotations in YOLO format, ideal for training object detection models.

---

## 📸 Output Sample

> 🔍 Face regions are scanned individually.  
> ✅ Acne spots are marked with bounding boxes.  
> 📊 Summary includes region-wise acne counts and total severity.


---


## 📄 License

This project is licensed under the MIT License.
