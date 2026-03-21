# ProjectRoute

<p align="center">
  <img src="https://img.shields.io/badge/Stack-MERN-brightgreen?style=for-the-badge" alt="MERN Stack">
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react" alt="React">
  <img src="https://img.shields.io/badge/Node.js-Express-339933?style=for-the-badge&logo=node.js" alt="Node.js">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb" alt="MongoDB">
</p>

<p align="center">
  Academic Project Management System — Streamlining student projects from proposal to completion
</p>

---

## 🔗 Live Demo

> **Note:** This is a private repository. Access to the full codebase available upon request.

**Demo Credentials:**
- Admin: `admin@projectroute.com` / `Admin@123`
- Teacher: `teacher@projectroute.com` / `Teacher@123`
- Student: `student@projectroute.com` / `Student@123`

---

## 📖 About

ProjectRoute is a comprehensive full-stack web application designed to digitize and automate academic project management. It serves as a centralized platform connecting students, teachers, and administrators in one unified ecosystem.

### What It Solves
- Manual supervisor allocation
- Scattered project submissions
- Inefficient deadline tracking
- Communication gaps between stakeholders

---

## 👥 User Roles

### 🎓 Student
- Submit project proposals with descriptions
- Request supervisor allocation
- Upload project files and documentation
- Track submission status and deadlines
- Receive and view supervisor feedback

### 👨‍🏫 Teacher / Supervisor
- Review supervisor requests from students
- Manage assigned student projects
- Provide structured feedback (positive, negative, general)
- Track project progress and status

### 👨‍💼 Administrator
- Manage all users (students, teachers, admins)
- Create and manage project deadlines
- Assign supervisors to students
- View analytics and statistics
- Broadcast system-wide notifications

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| **Role-Based Access Control** | Secure authentication with JWT and role-based routes |
| **Project Submission** | Students submit proposals with detailed descriptions |
| **Supervisor Management** | Request-based and manual supervisor assignment |
| **File Upload** | Cloud storage via Cloudinary for project files |
| **Deadline Tracking** | Global deadline management with notifications |
| **Feedback System** | Structured feedback from supervisors |
| **Email Notifications** | Automated email alerts via SMTP |
| **Analytics Dashboard** | Visual statistics for admins |
| **RESTful API** | Clean API architecture with Express |

---

## 🏗️ Architecture

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   React 19      │────▶│   Express API   │────▶│    MongoDB      │
│   (Frontend)    │◀────│   (Backend)     │◀────│    (Database)   │
└─────────────────┘     └────────┬────────┘     └─────────────────┘
                                 │
                    ┌────────────┴────────────┐
                    ▼                         ▼
            ┌──────────────┐          ┌──────────────┐
            │  Cloudinary  │          │   Nodemailer │
            │  (Files)     │          │   (Email)    │
            └──────────────┘          └──────────────┘
```

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| React 19 | UI Framework |
| Vite | Build Tool |
| Redux Toolkit | State Management |
| React Router v7 | Routing |
| Tailwind CSS | Styling |
| Recharts | Charts & Analytics |
| Axios | HTTP Client |

### Backend
| Technology | Purpose |
|------------|---------|
| Node.js | Runtime |
| Express 5 | Web Framework |
| MongoDB | Database |
| Mongoose | ODM |
| JWT | Authentication |
| bcrypt | Password Hashing |
| Cloudinary | File Storage |
| Nodemailer | Email Service |

---

## 📡 Sample API Endpoints

### Authentication
```
POST /api/v1/auth/register     - Register new user
POST /api/v1/auth/login        - Login user
POST /api/v1/auth/forgot       - Request password reset
```

### Projects
```
GET    /api/v1/project         - Get all projects
POST   /api/v1/project         - Create new project
GET    /api/v1/project/:id    - Get project by ID
PUT    /api/v1/project/:id    - Update project
DELETE /api/v1/project/:id    - Delete project
```

### Users
```
GET    /api/v1/admin/users     - Get all users
POST   /api/v1/admin/user      - Create user
PUT    /api/v1/admin/user/:id  - Update user
DELETE /api/v1/admin/user/:id  - Delete user
```

### Deadlines
```
GET    /api/v1/deadline        - Get all deadlines
POST   /api/v1/deadline        - Create deadline
PUT    /api/v1/deadline/:id    - Update deadline
DELETE /api/v1/deadline/:id    - Delete deadline
```

---

## 💡 Engineering Decisions

### JWT + HTTP-Only Cookies
Stateless authentication with JWT tokens stored in HTTP-only cookies provides CSRF protection while maintaining scalability across microservices.

### Cloudinary for Files
External file storage offloads bandwidth from the server, provides CDN acceleration, and offers image transformations.

### Redux Toolkit
Chosen for its simplified Redux patterns with `createSlice` and `createAsyncThunk`, reducing boilerplate while providing powerful DevTools.

### MongoDB with Indexing
Flexible schema design with strategic compound indexes ensures performant queries across complex relationships.

---

## ⚡ Performance Focus

- **Database Indexing** on frequently queried fields
- **Optimized Mongoose Queries** with selective population
- **API Rate Limiting** prevents abuse
- **Vite HMR** for instant development reloads
- **Production Build Optimization** with code splitting

---

## 🔮 Future Enhancements

- Real-time notifications (Socket.io)
- Student-supervisor chat system
- Plagiarism detection integration
- Mobile PWA
- Advanced analytics dashboard
- Team collaboration features

---

## 📬 Contact

**LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)

**GitHub:** [github.com/krishnamohan-vadlapatla](https://github.com/krishnamohan-vadlapatla)

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

<p align="center">Built with ❤️ using the MERN Stack</p>
