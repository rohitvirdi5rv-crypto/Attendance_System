
## 📋 Facial Recognition Attendance System

A **real-time AI-based attendance system** that uses **facial recognition** to automatically mark employee attendance. This project is built using **Streamlit** for the UI and integrates deep learning models like **FaceNet** for face recognition and **MTCNN** for face detection.

This system eliminates manual attendance and prevents proxy attendance using **biometric verification (face recognition).**

---

## 🚀 Key Features
* 👤 Employee Registration with Face Capture
* 🧠 AI-Based Face Recognition (FaceNet)
* 📸 Real-Time Camera Integration
* ⏱️ Automated Attendance Marking
* 🔐 Admin Authentication System
* 📊 Attendance Tracking & Reports (CSV-based)
* ⚙️ Customizable Attendance Time Slots
* 🗂️ Persistent Data Storage (CSV + JSON)
* 💻 Offline Executable Support (via cx_Freeze)

---

## 🧠 Tech Stack
* **Frontend/UI:** Streamlit
* **Face Detection:** MTCNN
* **Face Recognition:** FaceNet (Keras)
* **Backend Logic:** Python
* **Data Storage:** CSV & JSON
* **Model Handling:** TensorFlow, Keras

---

## 🧠 How the System Works (Architecture)

**1. Face Detection**

The system uses **MTCNN (Multi-task Cascaded Convolutional Networks)** to detect faces in real-time from the webcam.

**2. Feature Extraction (Face Embedding)**

Once a face is detected:

* It is resized to **160x160 pixels**
* Passed into **FaceNet**
* A **128D embedding vector** is generated

**3. Face Matching**

* The captured embedding is compared with stored embeddings
* Uses **Cosine Similarity**
* If similarity ≥ threshold (0.7), face is recognized

**4. Attendance Logic**

* Attendance is marked based on **current system time**
* Supports:
  - ✅ IN attendance
  - ✅ Half-day
  - ✅ OUT attendance

---

## 📁 Project Structure

<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/ea5957f7-e370-48dc-83cd-3d1d7cb4eb10" />

---

# ⚙️ System Workflow

## 🧾 Step 1: Admin Login

* Admin logs in using credentials
* Default:
```
Username: admin
Password: admin123
```
* Organizations Can Change the Username and Password
---

## 👤 Step 2: Employee Registration

* **1.** Click **Capture Face**
* **2.** System captures multiple frames
* **3.** Face embeddings are generated
* **4.** Employee details + embeddings are stored

---

## 📸 Step 3: Mark Attendance

* **1.** User opens **Mark Attendance**
* **2.** Webcam starts capturing frames
* **3.** Face is detected and encoded
* **4.** Matching happens with stored embeddings
* **5.** f match found → attendance marked

---

## ⏱️ Step 4: Time-Based Attendance

Attendance is marked based on configured time slots:

* IN Time
* Half-Day Time
* OUT Time

Stored in:
```
Data/time_config.json
```

---

# 📦 Installation & Setup

## 🚀 Option 1: Run Without Setup (Recommended)

A standalone executable (**run_app.exe**) has been provided so that this project can run locally on your system without any installation or configuration.

## 📥 Download

Download the application from the link below:

👉 https://github.com/rohitvirdi5rv-crypto/Facial_Recognition_Attendance_System/releases/download/v1.0/exe.win-amd64-3.11.rar

---

## ▶️ Steps to Run
* **1.** Download the file from the link above.
* **2.** Extract the downloaded archive.
* **3.** Open the extracted folder.
* **4.** Double-click on:
```
run_app.exe
```

The application will start automatically.

---

## ⚠️ Windows Security Warning

While running the application, Windows may display a warning such as “Windows protected your PC.”

This occurs because the application is not digitally signed. It is a common behavior for self-developed applications packaged using tools like **cx_Freeze**, and does not indicate that the file is harmful.

To proceed:

* Click **“More info”**
* Then select **“Run anyway”**

✅ The application is safe to use.

---

## ✅ Benefits
* No installation required
* No Python setup needed
* Ready to use immediately

---

## 💻 Option 2: Run Using Source Code (Manual Setup)

Use this if you want to run manually.

## 1. Download the repository

It will be downloaded in Zip file so you have to **Extract** the files. A direct link to the repository is available below or click on given **link** and you will be redirected to the repository.

[https://github.com/rohitvirdi5rv-crypto/Facial_Recognition_Attendance_System.git](https://github.com/rohitvirdi5rv-crypto/Facial_Recognition_Attendance_System.git)

---
## 2. Create a virtual environment

```
python -m venv venv
```
---
## 3. Activate Environment

Activate it on Windows:
```
venv\Scripts\activate
```
---

## 4️. Install Dependencies
```
pip install -r requirements.txt
```
---
## 5. Run the Streamlit app

```
streamlit run app.py
```

The application will open in your browser.

---
# 🧠 Important Concepts Explained
## 🔍 Face Embeddings

A face is converted into a numerical vector:

* Example: [0.12, -0.98, 0.45, ...]
* These embeddings are compared mathematically
---
## 📐 Cosine Similarity

Used to measure similarity between two faces:
```
1 → Perfect match  
0 → No similarity 
```
---
## 🎯 Threshold
* If similarity ≥ 0.7 → Face recognized
* Else → Face rejected
---

## 🔐 Security Features
* Admin login authentication
* Face-based biometric verification
* Prevention of duplicate attendance
* Time-based restrictions
---

## ⚡ cx_Freeze (EXE Creation)

This project supports **desktop executable creation.**

**Why** ```setup.py```**?**
* Converts Python project into ```.exe```
* Bundles dependencies
* Makes project portable

**Why** ```run_app.py```**?**
* Entry point for executable
* Launches Streamlit automatically
---

## 🚫 .gitignore Explanation

Prevents unnecessary files from being uploaded:

* ```venv/``` → virtual environment
* ```build/```, ```dist/``` → compiled files
* ```__pycache__/``` → cache files
* ```.egg-info/``` → package metadata
---
## 📌 Future Enhancements
* 🔐 Anti-spoofing detection (liveness detection)
* ☁️ Cloud database integration
* 📱 Mobile application
* 📊 Dashboard analytics
* 🧠 Improved recognition accuracy
* 🌐 Multi-device support
---
## 💡 Pro Tips
* Capture faces in good lighting
* Register multiple angles of the same person
* Avoid blurry images
* Keep face centered
---
## 👨‍💻 Author

**Rohit Virdi**

- BCA + MCA Graduate  
- Aspiring **Data Analyst / Data Scientist**  
- Skilled in **Python, Numpy, Pandas, SQL, Data Analysis, Machine Learning, Deep Learning, NLP and Visualization**  
- Interested in building data-driven solutions and intelligent systems  

🔗 GitHub: https://github.com/rohitvirdi5rv-crypto