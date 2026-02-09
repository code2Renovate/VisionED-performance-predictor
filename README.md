# 🎓 VisionED – AI-Powered Student Performance Predictor

VisionED is a full-stack **Student Performance Prediction System** built using **Flask** and **Machine Learning (Random Forest Regressor)**.

This project was developed as a **Minor Project** for  
**New Government Polytechnic, Patna-13 (NGP)**.

The system predicts end-semester academic outcomes (marks and attendance) based on students' academic performance.  
The prediction model is trained using structured historical data (subject marks and attendance) from previous batches of students.

VisionED provides a structured academic platform for administrators, teachers, and students. It includes model training, performance analysis, study material management, announcements, and academic query handling.

---

## 🚀 Key Features

### 👨‍🎓 For Students

- 🤖 AI-powered end-semester marks & attendance prediction  
- 📊 Performance analysis dashboard  
- 📝 Input academic data (internal marks, previous semester marks, previous semester attendance)  
- 📈 Real-time prediction results  
- 📚 Access study materials uploaded by teachers  
- 📢 View branch & semester specific announcements  
- ❓ Submit academic queries  

---

### 👨‍🏫 For Administrators / Teachers

- 👥 Manage students and administrators (View / Edit / Delete)
- 📂 Select Branch & Semester for model setup
- 📥 Download system-generated structured CSV template
- 🧠 Upload historical student data (marks + attendance)
- 🔄 Train branch-specific ML models dynamically
- 📚 Upload study materials for students
- 📢 Post announcements
- ❓ Respond to student queries
- 📊 Monitor prediction analytics
- 🛡 Super Admin verification system

---

## 🖼️ Application Screenshots

### 🏠 Home Page
Landing page with role-based login & signup system.

![Home Page](https://github.com/user-attachments/assets/7b978ae6-47e2-47e2-88cd-7ee0cb9aeb0a)

---

### 🎓 Student Dashboard
Students can access prediction analysis, study materials, announcements, and queries.

![Student Dashboard](https://github.com/user-attachments/assets/66e50bfd-ace5-4bf7-9768-f994de18d9eb)

---

### 👨‍🏫 Admin Dashboard
Control panel to manage users, upload academic data, and train models.

![Admin Dashboard](https://github.com/user-attachments/assets/30b4d22d-023b-4db6-b105-40ad22b07de9)

---

### 📂 Analytics Data Uploader
Admin selects **Branch & Semester**, downloads the structured template, fills previous batch data (marks & attendance), and uploads it to train the model.

![Analytics Uploader](https://github.com/user-attachments/assets/656003a4-3915-4a32-ab34-de07cadf517b)

---

### 📊 Performance Analytics – Part 1
Subject-wise prediction results generated using Random Forest Regression.

![Performance Analysis 1](https://github.com/user-attachments/assets/9fe392da-4d74-4585-a3f5-3625c9a31302)

---

### 📊 Performance Analytics – Part 2
Detailed analytics insights based on student academic inputs.

![Performance Analysis 2](https://github.com/user-attachments/assets/8a65b4ab-f507-4e76-bd76-2d56d18f750e)

---

### 👥 Registered Users Management
Admin interface to manage students and other administrators.

![Registered Users](https://github.com/user-attachments/assets/5d2983e1-2b60-4f4a-b52c-4547c79ff876)

---

## 🛠️ Tech Stack

### 🔙 Backend
- Python
- Flask
- Flask-SQLAlchemy
- Werkzeug

### 🤖 Machine Learning
- Scikit-learn (Random Forest Regressor)
- Pandas
- NumPy
- OpenPyXL

### 🎨 Frontend
- HTML5
- CSS3
- Bootstrap 5
- JavaScript

### 🗄 Database
- SQLite

---

## 🤖 Machine Learning Approach

The system uses a Random Forest Regressor to predict academic performance metrics.

### 📥 Input Features
- Previous Semester Marks
- Previous Semester Attendance Percentage
- Internal Subject Marks (entered by students during prediction)

### 🎯 Target Variables
- Final End-Semester Marks
- Final End-Semester Attendance

The model is trained separately for each Branch and Semester using structured historical academic data from previous batches.

Once trained, the model predicts both expected end-semester marks and expected attendance based on student academic inputs.

---

## 📂 Project Structure

```text
VisionED-performance-predictor/
│
├── static/
│   └── uploads/
│       └── images/
│           ├── admin_default.png
│           ├── student_default.png
│           └── profile images...
│
├── templates/
│   ├── admin_dashboard.html
│   ├── admin_material_uploader.html
│   ├── admin_announcements.html
│   ├── registered_users.html
│   ├── student_dashboard.html
│   ├── student_analytics.html
│   ├── profile_student.html
│   ├── profile_admin.html
│   ├── login.html
│   ├── signup.html
│   ├── index.html
│   ├── contact.html
│   ├── blog.html
│   ├── faq.html
│   ├── privacy.html
│   ├── team.html
│   └── other templates...
│
├── app.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/code2Renovate/VisionED-performance-predictor.git
cd VisionED-performance-predictor
```

---

### 2️⃣ Create Virtual Environment

#### Windows
```bash
python -m venv venv
venv\Scripts\activate
```

#### macOS / Linux
```bash
python3 -m venv venv
source venv/bin/activate
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Configure Secret Key

Open `app.py` and update:

```python
app.secret_key = "your_strong_secret_key_here"
```
🔐 This key is used to:
- Secure login sessions
- Protect admin authentication
- Prevent session tampering
- Enable flash messages

Replace it with a strong random string  
⚠️ If this key changes later, all users will be logged out automatically.  

---

### 5️⃣ Default Admin Codes (First Run)

- Admin Signup Code: `1234`
- Super Admin Code: `5678`

These can be changed from the Admin Profile page.

---

### 6️⃣ Run the Application

```bash
python app.py
```

---

### 7️⃣ Open in Browser

```
http://127.0.0.1:5000/
```

---

## 🔄 System Workflow
The following diagram illustrates how users navigate through the system and how workflows are connected:

![Workflow diagram](https://github.com/user-attachments/assets/23a00a5b-0e33-47ed-9945-04fdd4c3ac4a)

### 👨‍🏫 Teacher / Administrator Workflow

#### 🔐 Step 1: Registration & Access
1. Register using the provided Admin Code
2. Login to the system
3. Complete required profile details
4. Access the Admin Dashboard

⚠ Profile completion is required to access dashboard features.

---

#### 📊 Step 2: Upload Historical Academic Data

1. From the Admin Dashboard, navigate to **Material Uploader**
2. Select **Upload Analytics Data**
3. Choose:
   - Branch
   - Semester
4. Download the structured CSV template generated by the system

The template includes required columns such as:
- Previous Semester Marks
- Attendance Percentage
- Final End-Semester Marks

---

#### 📂 Step 3: Train the Prediction Model

1. Fill the CSV template with historical data of previous student batches
2. Ensure correct column structure
3. Upload the completed CSV file
4. The system trains the Random Forest model for the selected Branch & Semester

Once uploaded successfully, the system becomes ready to generate predictions for students of that branch and semester.

---

#### 📚 Teacher Dashboard Capabilities

After profile completion, teachers can:

- 📂 Upload study materials (Branch & Semester specific)
- 📢 Post announcements (Post / Edit / Delete)
- ❓ Solve student queries
- 👥 Manage registered users (View / Edit / Delete)
- 📊 View student prediction analytics
- 🛡 Super Admin privileges (Edit / Block / Delete Admins)

---

### 👨‍🎓 Student Workflow

#### 🔐 Step 1: Registration & Access
1. Register as a Student
2. Login to the system
3. Complete academic profile:
   - Branch
   - Semester

⚠ Profile completion is required to access dashboard features.

---

#### 📈 Step 2: Performance Analysis

Navigate to **Performance Analysis** and enter:

- Internal Subject Marks
- Previous Semester Marks
- Previous Semester Attendance Percentage

---

#### 🤖 Step 3: AI-Based Prediction

1. Submit the academic inputs
2. The system uses the trained Random Forest model
3. 3. Predicted End-Semester Marks and End-Semester Attendance are displayed

---

#### 📚 Student Dashboard Features

After profile completion, students can:

- 📊 Perform performance analysis
- 📂 View & Download study materials uploaded by teachers
- 📢 View announcements
- ❓ Ask academic queries
- 👍 Interact with posts (Like / Dislike / Reply)

---

## 🎯 Project Objective
VisionED aims to:
- Identify students at academic risk early
- Provide AI-based insights
- Improve academic decision making
- Digitize academic analytics in institutions

---

## 🏫 Academic Submission

Developed as a Minor Project for  
**New Government Polytechnic, Patna-13**
