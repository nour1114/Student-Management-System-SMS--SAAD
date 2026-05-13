# 🎓 Student Management System (SMS)

> A web-based information system designed to automate and streamline academic and administrative activities in universities and educational institutions.

**Course:** System Analysis & Design  
**Prepared by:** Nour Elsayed Elsbaay & Malak Mohamed Sorour  
**Group:** 4C | Instructor: Ahmed El-Sayed

---

## 📌 Overview

The Student Management System (SMS) replaces fragmented, manual university processes with a centralized digital platform. Students, instructors, and administrators can interact through a single system that handles everything from course registration to grade management and financial reporting.

---

## 🚩 Problem Statement

Many universities still rely on disconnected or partially manual systems, leading to:

- Difficulty managing large volumes of student data
- Delays and errors during course registration
- Inaccurate grade calculation and attendance tracking
- Poor inter-departmental communication
- Data duplication and information loss
- Lack of centralized reporting and analytics

---

## 🎯 Objectives

1. Digitize and centralize all student records
2. Simplify and automate the course registration process
3. Automate attendance and grade management
4. Improve communication between students, instructors, and administrators
5. Reduce paperwork and manual processing
6. Generate academic and financial reports automatically
7. Enhance data accuracy and security
8. Support decision-making through statistical reports

---

## 👥 System Users

| User Type | Responsibilities |
|-----------|-----------------|
| **Students** | Register courses, view grades, attendance, schedules, and transcripts |
| **Instructors** | Upload grades, manage attendance, and monitor student performance |
| **Administrators** | Manage students, courses, schedules, payments, and reports |

---

## ⚙️ Functional Requirements

### Student Functions
- Secure account registration and login with password recovery
- Browse and enroll in available courses (with prerequisite checks and duplicate prevention)
- View grades, GPA, attendance, course schedules, and academic transcripts
- Upload payment receipts and view payment confirmations

### Instructor Functions
- Record and track attendance; auto-generate attendance reports
- Upload grades; system auto-calculates final grades
- Monitor student performance and view course statistics

### Administrator Functions
- Full CRUD operations on student records and courses
- Assign instructors to courses
- Manage academic schedules and classroom allocations
- Auto-generate GPA, attendance, financial, and statistical reports
- Centralized database management with backup and recovery support

---

## 🔒 Non-Functional Requirements

| Category | Key Requirements |
|----------|----------------|
| **Performance** | Response time ≤ 2 seconds; supports concurrent users |
| **Security** | Authentication, role-based access control, data encryption |
| **Reliability** | ≥ 99% uptime; automatic backups; data recovery |
| **Usability** | Simple UI; mobile-friendly; accessible to non-technical users |
| **Scalability** | Supports growing student populations; modular architecture |
| **Availability** | 24/7 access with minimal maintenance downtime |

---

## 📊 System Diagrams

The project includes the following UML and process diagrams:

- **Use Case Diagram** — Shows interactions between Students, Instructors, and Administrators
- **Activity Diagram** — Models the student registration flow with validation logic
- **Context Diagram (Level 0)** — System boundary showing external entities (Student, Admin, Instructor, Payment System)
- **Level 1 DFD** — Decomposes the system into four main processes: Manage Students, Manage Courses, Manage Enrollment, Manage Grades
- **Level 2 DFD** — Drills into the Manage Enrollment process (Check Student Validity → Check Course Availability → Register Course → Update Enrollment Record)

---

## 🧠 Process Logic

### Structured English — Process 3: Manage Enrollment
```
BEGIN
  RECEIVE enrollment request
  CHECK if student exists
  IF student exists THEN
    CHECK course availability
    IF course available THEN
      REGISTER student
    ELSE
      DISPLAY "course not available"
    END IF
  ELSE
    DISPLAY "student not found"
  END IF
  STORE enrollment data
END
```

### Decision Table

| Condition | Rule 1 | Rule 2 | Rule 3 |
|-----------|--------|--------|--------|
| Student exists? | Yes | Yes | No |
| Course available? | Yes | No | — |
| **Register student** | ✔ | ✖ | ✖ |

---

## 📂 Data Dictionary

### Key Data Elements

| Element | Description | Type | Example |
|---------|-------------|------|---------|
| Student_ID | Unique student identifier | Integer | 20230045 |
| Course_ID | Unique course code | String | CS101 |
| Grade | Student final grade | String | A |

### Data Stores

| Store | Description |
|-------|-------------|
| Student Database | Stores student personal and academic info |
| Course Database | Stores course details and assignments |
| Grades Database | Stores grades linked to student and course IDs |

---

## 🗓️ Project Plan

The project follows a 7-phase plan executed from **March 5, 2026 to April 22, 2026**.

| Phase | Tasks | Duration |
|-------|-------|----------|
| 1. Initiation | Project Planning, Feasibility Study | 4 days |
| 2. Requirements | Requirements Gathering, System Analysis | 5 days |
| 3. Design | Database Design, System Architecture, UI/UX | 22 days |
| 4. Development | Frontend, Backend, Database Implementation | 22 days |
| 5. Testing | Unit, Integration, and System Testing | 5 days |
| 6. Deployment | Deployment, User Training | 4 days |
| 7. Maintenance | Maintenance & Support | 10 days |

---

## 💰 Financial Feasibility

### Development Cost Breakdown (EGP)

| Resource | Details | Cost |
|----------|---------|------|
| Developers (×3) | 4 months × 10,000/month | 120,000 |
| Tester (×1) | 2 months × 8,000/month | 16,000 |
| Designer (×1) | 5 months × 9,000/month | 45,000 |
| Server & Hosting | — | 20,000 |
| Software Tools | — | 10,000 |
| **Total Investment** | | **211,000 EGP** |

### Payback Analysis

- **Annual Revenue:** 90,000 EGP/year (university licensing fee)
- **Payback Period:** ~2.34 years (≈ 2 years and 4 months)
- **Annual Maintenance Cost:** 20,000 EGP/year

| Year | Cash Inflow (EGP) | Cumulative Cash Flow (EGP) |
|------|-------------------|---------------------------|
| 1 | 90,000 | 90,000 |
| 2 | 90,000 | 180,000 |
| 3 | 90,000 | 270,000 |

---

## ✅ Conclusion

The Student Management System provides a secure, efficient, and centralized platform that supports digital transformation in higher education. By replacing manual workflows with automation, it reduces operational costs, minimizes human error, and improves the academic experience for students, instructors, and administrators alike.
