# 🚀 GenAI Full Stack Job Preparation Web Application

A **Production-Ready Full Stack Generative AI Job Preparation Web Application** built with **React.js, Node.js, Express.js, MongoDB, JWT, Gemini AI, and Puppeteer**.

This application simulates a real-world AI-powered career platform where users can authenticate securely, upload their resumes, analyze job requirements, identify skill gaps, generate AI-powered interview preparation reports, and create ATS-optimized resumes in PDF format.

---

## 📌 Project Overview

The goal of this project is to combine **Full Stack Web Development + Generative AI** into a practical, real-world application.

The platform helps job seekers prepare for interviews by using AI to analyze their resume and job-related information.

### 🔥 Key Features

* 🔐 Secure user authentication
* 🔑 JWT-based authentication
* 🚫 JWT token blacklisting during logout
* 👤 User profile / GetMe API
* 📄 Resume upload and processing
* 🤖 Gemini AI integration
* 🧠 AI-powered resume analysis
* 📊 Skill extraction and skill-gap detection
* 💼 Job/interview preparation reports
* ❓ AI-generated interview questions
* 📑 ATS-optimized resume generation
* 🖨️ Dynamic PDF generation using Puppeteer
* 🔒 Protected frontend routes
* 🌐 REST API architecture
* 📱 Responsive React UI
* 📋 Recent interview reports
* 🔄 Report rehydration and state management

---

# 🛠️ Tech Stack

## Frontend

* React.js
* Vite
* React Router
* Axios
* Context API
* Custom Hooks
* CSS

## Backend

* Node.js
* Express.js
* REST APIs
* Multer
* Zod

## Database

* MongoDB
* MongoDB Atlas
* Mongoose

## Authentication & Security

* JWT
* HTTP Cookies
* Token Blacklisting
* Authentication Middleware
* Protected Routes
* CORS

## Generative AI

* Google Gemini API
* AI-powered resume analysis
* Skill extraction
* Skill-gap detection
* Interview question generation
* AI-generated resume content

## PDF Generation

* Puppeteer
* HTML → PDF generation

## API Testing

* Postman

---

# 🏗️ Application Architecture

The project follows a layered full-stack architecture.

```text
                    ┌─────────────────────┐
                    │      React.js       │
                    │      Frontend       │
                    └──────────┬──────────┘
                               │
                               │ Axios / REST API
                               ▼
                    ┌─────────────────────┐
                    │   Express.js API    │
                    │      Backend        │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
        Authentication     Gemini AI        MongoDB
             JWT          AI Processing     Database
              │                │                │
              └────────────────┼────────────────┘
                               │
                               ▼
                         Puppeteer
                               │
                               ▼
                         Resume PDF
```

---

# ✨ Main Features

## 🔐 Authentication

The application implements secure authentication using:

* User registration
* User login
* JWT authentication
* HTTP cookies
* Authentication middleware
* Protected routes
* GetMe API
* Logout functionality
* JWT token blacklisting

This provides a realistic authentication architecture similar to production applications.

---

## 🤖 Generative AI Integration

The application integrates **Google Gemini AI** to provide intelligent job-preparation functionality.

The AI can process user-provided information and generate:

* Interview preparation reports
* Interview questions
* Resume analysis
* Skills
* Missing skills
* Skill gaps
* Resume content
* ATS-friendly resume information

---

## 📄 Resume Processing

Users can upload their resumes through the application.

The backend processes the uploaded file and sends relevant information to the AI service.

### Resume Processing Flow

```text
User uploads Resume
        ↓
Frontend
        ↓
Multer File Upload
        ↓
Backend
        ↓
Resume Processing
        ↓
Gemini AI
        ↓
Extract Skills & Information
        ↓
Skill Gap Analysis
        ↓
Interview Preparation Report
```

---

# 🧠 AI-Powered Skill Gap Detection

One of the major features of the application is identifying the difference between the user's current skills and the skills required for a particular job.

### Example

```text
User Skills:

Python
SQL
Pandas
Machine Learning

Job Requirements:

Python
SQL
Machine Learning
React
Node.js
Docker
AWS

             ↓

AI Skill Gap Analysis

Missing Skills:

React
Node.js
Docker
AWS
```

This allows users to understand **what they need to learn to become more suitable for a particular role.**

---

# 🎯 AI Interview Preparation

The application generates interview preparation reports using Gemini AI.

The AI can generate:

* Technical interview questions
* Role-specific questions
* Skill-based questions
* Resume-based questions
* Interview preparation information

Users can access previously generated reports through the **Recent Reports** feature.

---

# 📊 Interview Reports

Interview reports are stored in MongoDB and can be retrieved using APIs.

The application supports:

* Generate report
* Get report by ID
* Get all reports
* Store report data
* Display recent reports
* Rehydrate report state

---

# 📑 ATS-Optimized Resume Generation

The application can generate resume content optimized for Applicant Tracking Systems (ATS).

The generated resume is converted into a PDF using **Puppeteer**.

### AI → PDF Pipeline

```text
User Data
   ↓
Gemini AI
   ↓
AI Generated Resume Content
   ↓
HTML Template
   ↓
Puppeteer
   ↓
PDF
   ↓
ATS-Optimized Resume
```

---

# 🖨️ PDF Generation with Puppeteer

Puppeteer is used to dynamically generate PDF resumes from HTML.

The backend:

1. Receives resume information
2. Generates the resume structure
3. Creates HTML
4. Launches Puppeteer
5. Converts HTML into PDF
6. Returns the generated PDF

---

# 📂 Project Structure

A simplified structure of the application:

```text
genai-fullstack-project/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── features/
│   │   │   ├── auth/
│   │   │   └── interview/
│   │   ├── hooks/
│   │   ├── context/
│   │   ├── pages/
│   │   ├── services/
│   │   └── App.jsx
│   │
│   └── package.json
│
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── services/
│   ├── utils/
│   ├── config/
│   ├── app.js
│   └── server.js
│
├── README.md
└── package.json
```

> The exact folder structure may vary depending on implementation.

---

# 🔄 Application Flow

```text
                    User
                     │
                     ▼
              Register / Login
                     │
                     ▼
              JWT Authentication
                     │
                     ▼
                Home Page
                     │
                     ▼
              Upload Resume
                     │
                     ▼
            Enter Job Information
                     │
                     ▼
                 Gemini AI
                     │
          ┌──────────┼──────────┐
          ▼          ▼          ▼
       Resume      Skills     Skill Gap
       Analysis   Extraction   Detection
          │          │          │
          └──────────┼──────────┘
                     ▼
          Interview Preparation
                     │
                     ▼
              Interview Report
                     │
                     ▼
           ATS Resume Generation
                     │
                     ▼
               Puppeteer
                     │
                     ▼
                 PDF Resume
```

---

# 🔑 Important Backend Concepts

This project demonstrates several real-world backend concepts:

### Authentication

```text
Register
   ↓
Login
   ↓
Generate JWT
   ↓
Store Token in Cookie
   ↓
Authentication Middleware
   ↓
Protected API
```

### Logout

```text
Logout
   ↓
JWT extracted
   ↓
Token added to Blacklist
   ↓
Cookie cleared
   ↓
Token cannot be reused
```

---

# 🧪 API Testing

The backend APIs were tested using **Postman**.

Examples of API operations include:

```text
POST   /auth/register
POST   /auth/login
POST   /auth/logout
GET    /auth/me

POST   /interview/generate
GET    /interview/:id
GET    /interview/reports

POST   /resume/generate
```

> Endpoint names may vary depending on the final implementation.

---

# ⚙️ Installation & Setup

## 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

## 2. Navigate to the Project

```bash
cd genai-fullstack-project
```

## 3. Install Dependencies

### Backend

```bash
cd backend
npm install
```

### Frontend

```bash
cd frontend
npm install
```

---

# 🔐 Environment Variables

Create a `.env` file inside the backend directory.

Example:

```env
PORT=5000

MONGODB_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

GEMINI_API_KEY=your_gemini_api_key

CLIENT_URL=http://localhost:5173
```

⚠️ **Never upload your `.env` file or API keys to GitHub.**

Add the following to `.gitignore`:

```gitignore
.env
node_modules/
```

---

# ▶️ Running the Application

## Start Backend

```bash
cd backend
npm run dev
```

## Start Frontend

Open another terminal:

```bash
cd frontend
npm run dev
```

The application will typically be available at:

```text
Frontend:
http://localhost:5173

Backend:
http://localhost:5000
```

---

# 📚 What I Learned From This Project

This project helped demonstrate practical knowledge of:

* Full Stack Web Development
* React.js
* Node.js
* Express.js
* MongoDB
* REST APIs
* JWT Authentication
* Token Blacklisting
* HTTP Cookies
* Middleware
* Protected Routes
* React Context API
* Custom Hooks
* Axios
* File Uploads
* Multer
* Zod Validation
* Gemini AI API Integration
* Prompt-based AI processing
* Resume parsing
* Skill extraction
* Skill-gap analysis
* AI-generated interview questions
* ATS resume generation
* Puppeteer
* Dynamic PDF generation
* Postman API testing
* Production-oriented project architecture

---

# 🎓 Project Learning Timeline

Topic                                
| Project Introduction                 |
| Server Setup & Authentication        |
| MongoDB Atlas Setup                  |
| Database & User Schema               |
| Authentication Routes                |
| Register User                        |
| Login User                           |
| API Testing with Postman             |
| Logout, Cookies & Token Blacklisting |
| GetMe API & Auth Middleware          |
| React/Vite Frontend Setup            |
| React Router & Auth Pages            |
| Authentication UI                    |
| Service Layer & Context              |
| Custom Hooks                         |
| CORS & Protected Routes              |
| AI Feature Architecture              |
| Interview Report Model & Zod         |
| Interview APIs & File Upload         |
| Gemini AI Integration                |
| Frontend AI Integration              |
| Interview APIs & Reports             |
| Interview Hook                       |
| Report Generation & Rehydration      |
| Recent Reports                       |
| Resume PDF Generation                |
| PDF Backend Integration              |
| Resume PDF Frontend Integration      |
| Project Completion                   |

---

# 🚀 Future Improvements

Potential improvements for future versions:

* [ ] Job description URL analysis
* [ ] Multiple resume templates
* [ ] Resume scoring system
* [ ] AI mock interview with voice
* [ ] Real-time AI interview
* [ ] Interview performance analytics
* [ ] Job recommendation system
* [ ] LinkedIn profile analysis
* [ ] Resume version management
* [ ] Cloud deployment
* [ ] Docker support
* [ ] CI/CD pipeline
* [ ] Rate limiting
* [ ] Advanced logging and monitoring

---

# 👨‍💻 Author

**Sohail Ashraf**

Aspiring Software Engineer | Full Stack Developer | GenAI Enthusiast

---

# ⭐ Acknowledgement

This project was built as a learning project based on a full-stack Generative AI job-preparation application walkthrough by **Ankur Prajapati**.

The project was used to understand and practice real-world concepts involving **Full Stack Development, Generative AI, authentication, database design, file processing, and PDF generation**.

---

# 📜 Disclaimer

This repository is intended for **educational and portfolio purposes**.

API keys, passwords, database credentials, and other sensitive environment variables should never be committed to the repository.

---

## ⭐ If you find this project useful

Feel free to ⭐ star the repository and explore the implementation.
