# 📘 Note Module 11 – PH University  

This document outlines the **functional requirements**, **data models**, and **API endpoints** for the PH University academic management system.  

---

## 🔑 Functional Requirements  

### Authentication  
**Student**  
- Login and Logout securely  
- Update password  

**Faculty**  
- Login and Logout securely  
- Update password  

**Admin**  
- Login and Logout securely  
- Update password  

---

### 👤 Profile Management  
**Student**  
- Manage and update profile  
- Update specific fields  

**Faculty**  
- Manage and update profile  
- Update specific fields  

**Admin**  
- Manage and update profile  
- Update specific fields  

---

### 🎓 Academic Process  
**Student**  
- Enroll in offered courses for a specific semester  
- View class schedule  
- View grades  
- View notice board and events  

**Faculty**  
- Manage student grades  
- Access student personal and academic information  

**Admin**  
- Manage semester  
- Manage courses  
- Manage offered courses  
- Manage sections  
- Manage rooms  
- Manage buildings  

---

### 👥 User Management  
**Admin**  
- Manage multiple accounts  
- Block and unblock users  
- Change user passwords  

---

## 🗂 Data Models  

### Student  
```json
{
  "_id": "",
  "id": "", // generated
  "name": "",
  "gender": "",
  "dateOfBirth": "",
  "email": "",
  "contactNo": "",
  "emergencyContactNo": "",
  "presentAddress": "",
  "permanentAddress": "",
  "guardian": "",
  "localGuardian": "",
  "profileImage": "",
  "academicDepartment": "",
  "status": "",
  "isDeleted": false,
  "createdAt": "",
  "updatedAt": ""
}
Faculty
{
  "_id": "",
  "id": "", // generated
  "name": "",
  "role": "",
  "gender": "",
  "dateOfBirth": "",
  "email": "",
  "contactNo": "",
  "emergencyContactNo": "",
  "presentAddress": "",
  "permanentAddress": "",
  "profileImage": "",
  "academicFaculty": "",
  "academicDepartment": "",
  "status": "",
  "isDeleted": false,
  "createdAt": "",
  "updatedAt": ""
}

Admin
{
  "_id": "",
  "id": "", // generated
  "name": "",
  "designation": "",
  "gender": "",
  "dateOfBirth": "",
  "email": "",
  "contactNo": "",
  "emergencyContactNo": "",
  "presentAddress": "",
  "permanentAddress": "",
  "profileImage": "",
  "managementDepartment": "",
  "status": "",
  "isDeleted": false,
  "createdAt": "",
  "updatedAt": ""
}

User (Admin Account)
{
  "_id": "",
  "id": "", // generated
  "password": "",
  "needPasswordChange": false,
  "role": "",
  "isDeleted": false,
  "createdAt": "",
  "updatedAt": ""
}

 🔗 API Endpoints

User

- POST /user/create-student

- POST /user/create-faculty

POST /user/create-admin

Student

GET /students

- GET /students/:id

PATCH /students/:id

DELETE /students/:id

GET /students/my-profile

Faculty

GET /faculties

GET /faculties/:id

PATCH /faculties/:id

DELETE /faculties/:id

GET /faculties/my-profile

Admin

GET /admins

GET /admins/:id

PATCH /admins/:id

DELETE /admins/:id

GET /admins/my-profile

Authentication

POST /auth/login

POST /auth/refresh-token

POST /auth/change-password

POST /auth/forget-password

🗄️ Data Modeling – Embedded vs Referenced

Embedded → Best when data size is fixed.

Referenced → Best when data size is growing dynamically.............