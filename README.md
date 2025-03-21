# Real-Time Face Attendance System

## Introduction
The **Real-Time Face Attendance System** allows for automatic attendance marking using facial recognition. This project utilizes OpenCV, K-Nearest Neighbors (KNN) for facial recognition, and Python for data handling. The system captures live video from a webcam, recognizes the faces of individuals, and records their attendance by storing their names and timestamps in a CSV file.

## Objectives
- Develop a system to recognize faces in real-time using a webcam.
- Use machine learning (KNN) to match detected faces to known faces.
- Store the names and attendance timestamps in a CSV file.
- Display real-time attendance information and handle unknown faces.

## Technologies Used
- **Programming Language:** Python
- **Libraries/Frameworks:** OpenCV, NumPy, pickle, scikit-learn
- **Tools:** Jupyter Notebook, VS Code
- **Dataset:** Custom dataset collected from faces captured by webcam.

## Workflow

1. **Data Collection:**
   - A face detection model is used to capture and collect images of faces.
   - These images are cropped and resized to a consistent shape (100x100 pixels) for training.
   - The system collects 50 samples for each individual.
   
2. **Data Preprocessing:**
   - Face images are converted to grayscale.
   - A face cascade classifier is used to detect faces in the captured images.
   - The images are resized and stored in a structured format.

3. **Model Development:**
   - The system uses the **K-Nearest Neighbors (KNN)** algorithm for face recognition.
   - Faces are flattened into a vector format and used to train the KNN model.
   - The model is trained using the captured face images and their corresponding labels (names).

4. **Real-Time Face Recognition:**
   - The webcam continuously captures images of faces.
   - The model predicts the identity of each detected face.
   - If the predicted face is recognized, the system updates the attendance list by appending the name and current timestamp to a CSV file.
   - If the face is unrecognized, it is marked as "Unknown."

5. **Attendance Logging:**
   - Attendance is logged in a CSV file with the format `["NAME", "DATE_TIME"]`.
   - A new entry is created for each recognized face.
   - If a face is already logged for the current date, no duplicate entry will be made.

## Results
- The system uses real-time face detection and updates the attendance file as faces are recognized.
- Accuracy is highly dependent on lighting, camera quality, and the number of training samples for each person.

## Future Work
- Improve face recognition accuracy by using more advanced machine learning models (e.g., Deep Learning).
- Extend the system to work with multiple cameras or in different environments.
- Integrate the system with a web application for viewing and managing attendance logs.

## Conclusion
The **Real-Time Face Attendance System** is an effective and efficient way to track attendance using facial recognition technology. This system simplifies attendance marking, increases accuracy, and reduces the chances of errors in attendance logs. It can be adapted for use in various environments such as schools, offices, or events, enabling automatic and real-time attendance management. The system can be further improved with advanced techniques like deep learning for better accuracy and robustness.

## Clone Repository

To clone this repository to your local machine, run the following command:

```bash
git clone https://github.com/adnan-saif/Live-Face-Attendance-System.git
