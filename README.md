# 🧠 YOLOv3 Custom Object Detection with ImageAI

This Jupyter Notebook demonstrates how to train and use a custom object detection model using **ImageAI** and **YOLOv3**. It guides you through dataset setup, training, and object detection on images.

---

## 📓 Contents

- `ImageAI.ipynb` – Complete training and detection pipeline using YOLOv3  
- Built using the **ImageAI** library and a **custom dataset**  
- Outputs object predictions with bounding boxes and confidence scores  

---

## 📦 Dataset Used

This notebook was originally tested using a custom dataset named **`hololens-yolo.zip`**, designed for detecting Microsoft HoloLens in images.

> ❗ **Note**: This dataset is **not included** 

---

## 🛠️ Using Your Own Dataset

Yes! This notebook can be used to **train on any custom object detection dataset**, not just HoloLens.

To use your own dataset:

1. Prepare your dataset in the following folder structure:
    ```
    your-dataset-name/
    ├── train/
    ├── test/
    ├── json/                  # Contains the detection config
    └── models/                # Optionally include a pretrained YOLOv3 model
    ```

2. Zip the folder (e.g., `your-dataset-name.zip`)

3. In **Google Colab**, upload the zip file before running the notebook. You can do this by:
   - Clicking the 📁 file icon on the left sidebar
   - Clicking the 📤 upload button and selecting your `.zip` file
   - 
4. Update the filename in the notebook:
   ```python
   with zipfile.ZipFile('/content/your-dataset-name.zip', 'r') as zip_ref:
       zip_ref.extractall('/content/drive/MyDrive')
