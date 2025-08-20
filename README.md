# SecureMedAI

SecureMedAI is an AI-powered healthcare web platform that allows patients to predict possible diseases based on symptoms and seamlessly book appointments with specialized doctors. Built with a focus on real-time dashboards, smart doctor matching, and a user-centric experience.

---

## Overview

SecureMedAI bridges the gap between intelligent diagnosis and timely medical care. Patients receive instant predictions based on symptoms and are connected with top-rated, relevant doctors. Doctors manage appointments and access patient history, while admins oversee the platform.

The platform incorporates machine learning models tailored to user roles:

- **Patients** use a **Random Forest** model for client-side, symptom-based disease prediction.
- **Doctors** utilize **Federated Learning** for privacy-preserving, collaborative diagnosis improvement across distributed data sources.

---

## Features

### User Roles

- **Patient**:  
  - Symptom-based disease prediction using Random Forest  
  - Book appointments  
  - Rate doctors  
  - Chat securely  

- **Doctor**:  
  - Predict diseases using Federated Learning  
  - View and manage appointments  
  - Access patient information  
  - Communicate securely with patients  
  - Receive ratings  

- **Admin**:  
  - Manage platform users, doctors, and feedback  
  - View analytics and monitor system activity  

---

### Core Functionality

- Authentication and onboarding flow for Patients, Doctors, and Admins  
- AI-based disease prediction  
  - Random Forest (Patient-side)  
  - Federated Learning (Doctor-side)  
- Doctor appointment booking system  
- Doctor ratings and specialization filtering  
- Smart doctor matching based on prediction, rating, and availability  
- Advanced doctor search by:  
  - Experience  
  - Availability  
  - Languages spoken  
- Secure patient-doctor chat system  
- Real-time role-based dashboard  
- Mobile-responsive UI with a modern design  

---

## Tech Stack

| Layer            | Technology                       |
|------------------|----------------------------------|
| Frontend         | React.js, Tailwind CSS           |
| Backend          | Django REST Framework            |
| Database         | PostgreSQL                       |
| Authentication   | JWT, Django Authentication       |
| Charts           | Recharts, Chart.js               |
| ML Models        | Random Forest, Federated Learning|

---


## ⚙️ Installation & Setup

```bash
# Clone the repository
git clone ""
cd securemedai

# Database set up 
Create a **.env** file with the help of .env.example

# Frontend setup
cd frontend
npx update-browserslist-db@latest
npm install
npm start

# Backend setup
cd backend
python -m venv env
.\env\Scripts\activate  
pip install -r requirements.txt
python manage.py migrate
python manage.py create_test_users
python manage.py populate_diseases
python manage.py populate_doctors
python manage.py runserver