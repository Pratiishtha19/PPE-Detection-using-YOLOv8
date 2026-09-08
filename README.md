# 🦺 PPE Detection using YOLOv8

## 📌 Project Overview

**PPE Detection using YOLOv8** is an AI-based computer vision application developed using **Python, YOLOv8, Streamlit, Pillow, and NumPy**.

The application is designed to detect Personal Protective Equipment (PPE) in construction worker images. Users can upload an image through the Streamlit interface, and the trained YOLOv8 model analyzes the image and identifies the PPE detected.

The application displays the original image, the detection result with bounding boxes, and the detected PPE classes along with their confidence scores.

## 🎯 Objective

The main objective of this project is to understand how a **custom-trained YOLOv8 object detection model** can be integrated into a practical application for detecting Personal Protective Equipment in construction environments.

## ✨ Features

* 📤 Upload construction worker images
* 🤖 Detect PPE using a trained YOLOv8 model
* 🖼️ Display the original uploaded image
* 📦 Display detected PPE with bounding boxes
* 📊 Display detected PPE class names
* 📈 Display confidence scores
* ⚠️ Show a warning when no PPE is detected
* 🌐 Interactive web interface using Streamlit

## 🛠️ Technologies Used

| Technology             | Purpose                                                    |
| ---------------------- | ---------------------------------------------------------- |
| **Python**             | Main programming language                                  |
| **Streamlit**          | Creates the interactive web interface                      |
| **Ultralytics YOLOv8** | Performs PPE object detection                              |
| **Pillow (PIL)**       | Opens and handles uploaded images                          |
| **NumPy**              | Converts images into numerical arrays for model processing |

## 🧠 YOLOv8 Model

This project uses a **custom-trained YOLOv8 model** stored in:

```text
best.pt
```

Unlike a general pre-trained model, `best.pt` is the trained model used specifically for the PPE detection task.

The model is loaded using:

```python
model = YOLO("best.pt")
```

The uploaded image is converted into a NumPy array:

```python
img_array = np.array(image)
```

The array is then passed to the YOLO model:

```python
results = model(img_array)
```

The model detects objects and provides information such as:

* Object/class name
* Bounding box
* Confidence score

## 🔄 Application Workflow

```text
        User uploads image
                ↓
        Streamlit receives image
                ↓
         Pillow opens image
                ↓
      Image converted to NumPy
                ↓
       Custom YOLOv8 model
             processes image
                ↓
          PPE is detected
                ↓
       Bounding boxes generated
                ↓
       Detection result displayed
                ↓
  PPE names & confidence scores shown
```

## 📂 Project Structure

```text
PPE-Detection-YOLOv8/
│
├── app.py
├── best.pt
├── requirements.txt
└── README.md
```

> **Note:** If your actual Python file has a different name, replace `milestone 2.py` with your actual filename.

## ⚙️ Installation

### Step 1: Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_LINK
```

### Step 2: Navigate to the project folder

```bash
cd PPE-Detection-YOLOv8
```

### Step 3: Install the required libraries

```bash
pip install -r requirements.txt
```

The `requirements.txt` file should contain:

```text
streamlit
ultralytics
pillow
numpy
```

## ▶️ How to Run

Run the Streamlit application using:

```bash
streamlit run "app.py"
```

Replace `app.py` with the actual name of your Python file if different.

The application will open in your web browser.

## 📸 Screenshots

### Original Image

Add a screenshot showing the uploaded construction worker image.

### PPE Detection Result

Add a screenshot showing the detected PPE with bounding boxes.

### Detected PPE and Confidence

Add a screenshot showing the detected PPE classes and their confidence scores.

## 📚 Concepts Learned

Through this project, I learned:

* Python programming
* Computer Vision fundamentals
* Object Detection
* YOLOv8
* Custom-trained AI models
* Bounding boxes
* Confidence scores
* Image processing using Pillow
* NumPy arrays
* Streamlit application development
* Integrating trained AI models into applications
* Handling image uploads
* Displaying AI prediction results

## 🎓 Internship Learning

This project provided practical experience in applying **Artificial Intelligence and Computer Vision** to a real-world safety-related use case.

I learned how to integrate a custom-trained YOLOv8 model with a Streamlit application, process uploaded images, perform object detection, visualize predictions using bounding boxes, and display confidence scores to the user.

## 🚀 Possible Future Improvements

* Detect PPE from live camera/video streams
* Add real-time PPE monitoring
* Generate safety compliance reports
* Add alerts when required PPE is missing
* Store detection results for monitoring
* Deploy the application online
* Improve detection accuracy with a larger and more diverse dataset

## 👤 Author

**Pratishtha Gadwanshi**
