# 🧴 Acne Detection with YOLOv8 + MediaPipe (Full Pipeline)

This project provides a complete, deep learning-based pipeline to **detect acne across different facial regions** using **YOLOv8** and **MediaPipe Face Mesh**. It goes beyond binary classification by breaking the face into regions (cheeks, forehead, under-eyes) and detecting acne spots individually in each.

It includes:
- 📦 Dataset upload and extraction
- 🧠 YOLOv8 model training
- 📸 Face image upload and detection
- 📥 Model download for future use

---

## 🧠 What It Does

✅ Upload and process acne dataset (YOLOv8 format)  
✅ Automatically updates `data.yaml` paths after extraction  
✅ Trains a YOLOv8 model (`yolov8n.pt`) on the dataset  
✅ Uploads a user face image and detects acne  
✅ Divides the face into key regions using MediaPipe:
- Left Cheek
- Right Cheek
- Forehead
- Under Eyes  
✅ Detects acne spots in each region using the trained model  
✅ Shows acne count per region and **classifies severity**:
- `Clear`
- `Mild`
- `Moderate`
- `Severe`  
✅ Downloads the best-trained model (`best.pt`) at the end

---

## 📚 Dataset Used

**Kaggle Dataset**: [Acne Dataset in YOLOv8 Format](https://www.kaggle.com/datasets/osmankagankurnaz/acne-dataset-in-yolov8-format)

- Format: YOLOv8-compliant
- Includes: train/valid/test splits with bounding boxes for acne

---

## 🛠 Tech Stack

| Library         | Purpose                                |
|----------------|-----------------------------------------|
| 🔮 YOLOv8 (Ultralytics) | Object detection model (acne)      |
| 🟢 MediaPipe     | Detect facial landmarks and regions    |
| 🎨 OpenCV        | Image handling and preprocessing       |
| 📊 Matplotlib    | Visualization of results               |
| 📁 PyYAML        | Read and modify `data.yaml` file       |
| 🧪 Google Colab  | Runtime and interactive interface      |

---

## 🚀 How to Use (Colab)

> **Note:** This pipeline is designed for Google Colab usage.

1. **Upload your acne dataset ZIP** (from Kaggle)
2. The notebook extracts and updates the paths in `data.yaml`
3. YOLOv8 training starts using `yolov8n.pt`
4. Upload a **face image** (JPG or PNG)
5. Model detects acne region-wise using MediaPipe + YOLO
6. Results are displayed with bounding boxes and counts
7. You get a severity level + option to **download trained model**

---

## 🎯 Output Example

After running, you’ll get:

- 📸 An image with bounding boxes over acne spots
- 📊 A printed region-wise acne count
- 🚦 Severity level based on total detected spots

```text
Acne Distribution Summary:
LEFT_CHEEK: 2 acne spots
RIGHT_CHEEK: 4 acne spots
FOREHEAD: 1 acne spots
UNDER_EYES: 3 acne spots

Total acne detected: 10
Acne Severity: Moderate
