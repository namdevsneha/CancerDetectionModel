# Breast Cancer Segmentation from Ultrasound Images

This project is a **machine learning-powered web application** that detects and segments breast cancer regions from ultrasound images uploaded by users. It leverages a **UNet-based deep learning model** trained using the `segmentation_models` library. The solution includes:

- **ML model** for semantic segmentation of breast cancer in ultrasound images  
- **Frontend** built with **ReactJS** for an intuitive and interactive user experience  
- **Backend** using **Node.js** to handle model API requests, manage uploads to **Cloudinary**, and connect the frontend and model  
- **Cloudinary** integration for secure and scalable image storage  

## Features

- Upload ultrasound images via a web interface  
- Receive real-time predictions and segmented tumor regions  
- Visually compare original and segmented images  
- Secure cloud-based storage of inputs and results  

## Machine Learning Model

- **Architecture**: UNet with **ResNet34** as encoder  
- **Frameworks Used**: TensorFlow, Keras, segmentation_models  
- **Input Shape**: `(256, 256, 3)`  
- **Loss Functions**: Combined Dice Loss + Binary Focal Loss  
- **Metric**: Intersection over Union (IoU)  
- **Output**: Binary mask highlighting cancerous regions  

## Tech Stack

| Component    | Technology        |
|--------------|-------------------|
| Frontend     | ReactJS           |
| Backend      | Node.js, Express  |
| ML Model API | TensorFlow, Python|
| Image Upload | Cloudinary        |

## Directory Structure

CancerDetectionModel
- backend/
  
   | - python/
  
          |- segment.py

          |- segmentation_model
  
   | - routes/
  
          |- upload.js
  
   | - uploads/
  
   | - package-lock.json
  
   | - package.json
  
   | - server.js
  
- frontend/
  
  |- node_modules/

  |- public/

  |- src/

    |- assets/

    |- components/

      |- Navbar.jsx

      |- SessionContext.jsx

      |- App.css

      |- App.jsx

      |- HistoryPage.jsx

      |- Home.jsx

      |- index.css

      |- main.jsx

  |-.gitignore

  |- index.html

  |- package-lock.json

  |-package.json

  |- README.md

  |- vite.config.js


## Setup Instructions

### 1. Download the model from drive

(https://drive.google.com/file/d/1pQxTv3mST3qGhrqMjDmkNB8MRAotGQrj/view?usp=drive_link)
cd CancerDetectionModel

### 2. Run the Backend

cd backend
npm install
npx nodemon

### 3. Run the Frontend

cd frontend
npm install
npm run dev

##  Example Output

![image](https://github.com/user-attachments/assets/7b9ed6c1-90e4-4685-8928-975227929981)


##  Future Improvements

- Add user authentication  
- Keeping track of past user uploaded images
- Expand to other cancer types or imaging modalities  

##  License

This project is licensed under the MIT License.

