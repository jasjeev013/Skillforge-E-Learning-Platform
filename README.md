# 🎓 SkillForge E-Learning Platform

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![React](https://img.shields.io/badge/Frontend-React%20%7C%20Vite-61DAFB)
![Spring Boot](https://img.shields.io/badge/Backend-Spring%20Boot%203.5-6DB33F)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248)
![Java](https://img.shields.io/badge/Java-21-ED8B00)

**SkillForge** is a next-generation Learning Management System (LMS) designed to bridge the gap between traditional learning and AI-driven assessment. It provides a robust ecosystem for Instructors to craft course content, Students to learn and get certified via AI interviews, and Admins to oversee platform metrics.

Built with a modern **React (Vite)** frontend and a scalable **Spring Boot** backend.

---

## 🚀 Features

### 👨‍🏫 For Instructors
* **Course Management:** Create comprehensive courses with organized sections and topics.
* **Rich Media:** Upload learning materials (PDFs, Videos) securely via AWS S3.
* **Hybrid Assessments:** Create manual quizzes or utilize **Generative AI** to automatically create quizzes based on course content.
* **Publication Workflow:** Draft, review, and publish courses to the marketplace.

### 👨‍🎓 For Students
* **Progress Tracking:** Visual dashboards to track course completion and quiz scores.
* **Interactive Learning:** Clean, distraction-free learning interface with 3D elements.
* **AI Subjective Interview:** A unique feature where students face an AI-driven written interview upon course completion. The AI evaluates deep understanding rather than just multiple-choice answers.
* **Certification:** Automated certificate generation upon passing the AI Interview.

### 👮‍♂️ For Admins
* **Platform Dashboard:** High-level metrics, user trends, and enrollment statistics.
* **User Management:** Oversee instructors and students.
* **System Logs:** Monitor platform health and activities.

### 🔐 Security & Core
* **RBAC (Role-Based Access Control):** Strict separation of duties for Admin, Instructor, and Student.
* **Secure Authentication:** JWT (JSON Web Token) implementation with State Management.
* **Data Integrity:** Robust validation and error handling.

---

## 🛠 Tech Stack

### Frontend (Client)
* **Framework:** React 18 with TypeScript
* **Build Tool:** Vite
* **Styling:** Tailwind CSS, Shadcn/UI, Lucide React
* **3D Graphics:** Three.js (@react-three/fiber, @react-three/drei)
* **State & Data:** React Query (@tanstack/react-query), React Hook Form, Zod
* **HTTP Client:** Axios

### Backend (Server)
* **Framework:** Spring Boot 3.5.7
* **Language:** Java 21
* **Database:** MongoDB
* **Security:** Spring Security, JWT (jjwt)
* **Storage:** AWS S3 SDK
* **Documentation:** OpenApi (Swagger UI)
* **Utilities:** ModelMapper, Lombok, Jackson

---

## 📂 Project Structure

```text
jasjeev013-skillforge-e-learning-platform/
├── client/                 # React Frontend application
│   ├── src/
│   │   ├── components/     # Reusable UI components (Shadcn, 3D Hero)
│   │   ├── pages/          # Application views (Dashboards, Course Learn)
│   │   ├── services/       # API integration (Auth, Course, AI services)
│   │   └── hooks/          # Custom React hooks
│   └── ...
└── server/                 # Spring Boot Backend application
    ├── src/main/java/com/skillforge/platform/
    │   ├── config/         # Security, S3, and Swagger configs
    │   ├── controllers/    # REST API Endpoints
    │   ├── models/         # MongoDB Documents
    │   ├── services/       # Business Logic (AI, Quiz, Auth)
    │   └── payloads/       # DTOs (Data Transfer Objects)
    └── ...
````

-----

## ⚙️ Installation & Setup

### Prerequisites

  * Node.js (v18+)
  * Java JDK 21
  * MongoDB (Local or Atlas)
  * Maven

### 1\. Backend Setup (Spring Boot)

Navigate to the server directory:

```bash
cd server
```

Configure your environment variables in `src/main/resources/application.properties` (or create an `application.yml`):

```properties
spring.data.mongodb.uri=mongodb://localhost:27017/skillforge
spring.data.mongodb.database=skillforge
jwt.secret=YOUR_SUPER_SECRET_KEY_HERE
cloud.aws.credentials.access-key=YOUR_AWS_ACCESS_KEY
cloud.aws.credentials.secret-key=YOUR_AWS_SECRET_KEY
cloud.aws.region.static=us-east-1
# AI Service Configuration
ai.api.key=YOUR_AI_PROVIDER_KEY
```

Build and run the application:

```bash
./mvnw spring-boot:run
```

The server will start on `http://localhost:8080`.

### 2\. Frontend Setup (React)

Open a new terminal and navigate to the client directory:

```bash
cd client
```

Install dependencies:

```bash
npm install
```

Create a `.env` file in the `client` root:

```env
VITE_API_URL=http://localhost:8080/api
```

Run the development server:

```bash
npm run dev
```

The client will start on `http://localhost:5173`.

-----

## 📖 API Documentation

Once the backend is running, you can explore the full REST API documentation via Swagger UI:

👉 **[http://localhost:8080/swagger-ui/index.html](https://www.google.com/search?q=http://localhost:8080/swagger-ui/index.html)**

-----

## 📸 Screenshots

*(Add screenshots of your application here)*

| Landing Page | Student Dashboard |
|:---:|:---:|
| ![Logo](./images/landing.png) | ![Logo](./images/student.png) |

| Instructor Dashboard | Admin Dashboard |
|:---:|:---:|
| ![Logo](./images/instructor.png) | ![Logo](./images/admin.png) |

| Course Interface | AI Interview |
|:---:|:---:|
| ![Logo](./images/course.png) | ![Logo](./images/interview.png) |

-----

## 🤝 Contributing

Contributions are welcome\! Please follow these steps:

1.  Fork the repository.
2.  Create a feature branch (`git checkout -b feature/AmazingFeature`).
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4.  Push to the branch (`git push origin feature/AmazingFeature`).
5.  Open a Pull Request.

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

## 👤 Author

**Jasjeev**

  * GitHub: [jasjeev013](https://github.com/jasjeev013)
  * Project Link: [Skillforge-E-Learning-Platform](https://github.com/jasjeev013/Skillforge-E-Learning-Platform)
