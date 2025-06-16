# Face Recognition Attendance System 🧠📸

This project is a **Face Recognition Attendance System** built using Python. It captures faces using a webcam, recognizes known faces, and **marks attendance in a CSV file only if the person is present and recognized**.

---

## 🚀 Features

- Real-time face detection and recognition
- Attendance is automatically **marked only once per person per day**
- Data saved in a CSV file with name and timestamp
- Lightweight and easy to run on any system

---

## 💻 Technologies Used

- **Python 3**
- **OpenCV (`cv2`)** – for webcam access and image processing
- **face_recognition** – for facial feature detection and matching
- **NumPy** – for image array handling
- **os** – for file system operations
- **datetime** – for getting the current date and time
- **csv** – to write attendance records in a `.csv` file


---

## 🗂️ Project Structure

```bash
Face_Recognition_Attendance/
├── attendance system.ipynb   # Jupyter Notebook with full code and explanation
├── photos/                   # Folder containing known face images
├── Date.csv            # CSV file to store attendance (Name, Time)
├── README.md                 # Project documentation

