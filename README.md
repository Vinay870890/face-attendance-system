# Face Recognition Attendance System 🧠📸

![Python](https://img.shields.io/badge/Python-3.x-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-Enabled-green)
![face_recognition](https://img.shields.io/badge/face__recognition-library-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

A smart, real-time **Face Recognition Attendance System** built in Python. It uses your webcam to detect and recognize faces, then automatically marks attendance in a CSV file — with no manual entry, no duplicate records, and no paperwork.

---

## 📌 Overview

Traditional attendance systems rely on manual registers, ID cards, or biometric scanners that require extra hardware. This project solves that with just a webcam and Python.

The system:
1. Learns known faces from a folder of reference photos
2. Detects and recognizes faces live from the webcam feed
3. Marks attendance **automatically and only once per person per day**
4. Logs the result with a timestamp into a clean CSV file

It's lightweight, beginner-friendly, and runs entirely on your local machine — no cloud services or paid APIs required.

---

## 🚀 Features

- ✅ **Real-time face detection & recognition** using a live webcam feed
- ✅ **One entry per person per day** — duplicate detections are automatically ignored
- ✅ **Simple enrollment** — just drop a photo into the `photos/` folder to register a new person
- ✅ **Automatic CSV logging** with `Name` and `Time` columns
- ✅ **No internet or cloud dependency** — works fully offline
- ✅ **Lightweight & portable** — runs on most systems with a webcam
- ✅ **Readable, well-documented code** in a Jupyter Notebook for easy learning and customization

---

## 🧩 How It Works

```
        ┌────────────────────┐
        │   photos/ folder    │
        │ (known face images) │
        └─────────┬───────────┘
                   │  encode faces
                   ▼
        ┌────────────────────┐
        │  Face Encoding      │
        │  (face_recognition) │
        └─────────┬───────────┘
                   │
                   ▼
        ┌────────────────────┐
        │   Webcam Feed       │
        │   (OpenCV / cv2)    │
        └─────────┬───────────┘
                   │  detect + compare faces
                   ▼
        ┌────────────────────┐
        │   Match Found?       │
        └─────────┬───────────┘
             Yes   │   No
                   ▼
        ┌────────────────────┐
        │ Already marked      │──No──▶ Write Name + Time to CSV
        │ today?              │
        └─────────┬───────────┘
             Yes   │
                   ▼
             Skip (no duplicate)
```

---

## 💻 Technologies Used

| Technology | Purpose |
|---|---|
| **Python 3** | Core programming language |
| **OpenCV (`cv2`)** | Webcam access and image processing |
| **face_recognition** | Facial feature detection and matching |
| **NumPy** | Image array handling |
| **os** | File system operations (reading known faces, etc.) |
| **datetime** | Fetching current date and time for logging |
| **csv** | Writing attendance records to a `.csv` file |

---

## 🗂️ Project Structure

```bash
Face_Recognition_Attendance/
├── attendance system.ipynb   # Jupyter Notebook with full code and explanation
├── photos/                   # Folder containing known face images
├── Date.csv                  # CSV file storing attendance (Name, Time)
└── README.md                 # Project documentation
```

---

## ⚙️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/Face_Recognition_Attendance.git
   cd Face_Recognition_Attendance
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   venv\Scripts\activate      # Windows
   source venv/bin/activate   # macOS/Linux
   ```

3. **Install dependencies**
   ```bash
   pip install opencv-python face_recognition numpy
   ```

   > ⚠️ **Note:** `face_recognition` depends on `dlib`, which may require **CMake** and a **C++ compiler** installed on your system before it builds successfully. On Windows, installing the "Desktop development with C++" workload via Visual Studio Build Tools usually resolves build errors.

4. **Add known faces**
   Place a clear, front-facing photo of each person in the `photos/` folder, named after the person (e.g. `vinay.jpg`).

5. **Run the notebook**
   Open `attendance system.ipynb` in Jupyter Notebook or JupyterLab and run all cells.

---

## ▶️ Usage

1. Launch the notebook — this opens your webcam feed.
2. Stand in front of the camera; the system detects and identifies your face.
3. If recognized and not already marked for the day, your attendance is instantly logged.
4. Press **`q`** to close the webcam window.
5. Open `Date.csv` to view the attendance log.

---

## 📄 Sample Output (`Date.csv`)

| Name | Time |
|---|---|
| Vinay | 09:02:15 |
| Riya | 09:04:47 |
| Aman | 09:07:31 |

---

## 🔮 Future Enhancements

- 🌐 Web-based dashboard to view attendance records
- ☁️ Cloud/database integration (Firebase, MySQL, or MongoDB)
- 📱 Mobile app support
- 📧 Automatic email/SMS attendance reports
- 🛡️ Liveness detection to prevent spoofing with photos
- 👥 Multi-camera / multi-classroom support
- 📊 Monthly attendance analytics and reports

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repository, raise issues, or submit pull requests to improve functionality, accuracy, or add new features.

---

## 📜 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute it with attribution.

---

## 👨‍💻 Author

**vinay (Btech CS AI ML) , IIMT University, Meerut**


---

<p align="center">Made with Python, OpenCV, and a passion for automation 🚀</p>
