# 🛠️ Teknologi Stack - Ketua Tingkat App

## 🎨 Frontend

### Framework & Library
- **React.js** 18.x - UI library
- **TypeScript** - Type safety
- **Tailwind CSS** - Utility-first CSS
- **Vite** - Fast build tool
- **Redux Toolkit** - State management
- **React Router** - Navigation

### UI Components & Design
- **Shadcn/ui** - Headless UI components
- **Lucide React** - Icon library
- **Framer Motion** - Animations
- **React Hook Form** - Form management
- **Zod** - Schema validation

### Utilities
- **Axios** - HTTP client
- **Socket.io-client** - Real-time communication
- **Date-fns** - Date utilities
- **React Query** - Data fetching & caching

---

## 🔧 Backend

### Framework & Runtime
- **Node.js** 18.x - Runtime
- **Express.js** - Web framework
- **TypeScript** - Type safety

### Database
- **PostgreSQL** 14+ - Primary database
- **Prisma ORM** - Database ORM
- **Redis** - Caching & sessions

### Authentication & Security
- **JWT (jsonwebtoken)** - Token-based auth
- **bcryptjs** - Password hashing
- **helmet** - HTTP header security
- **cors** - Cross-origin resource sharing
- **express-rate-limit** - Rate limiting

### Real-time Communication
- **Socket.io** - WebSocket library
- **Socket.io-redis** - Adapter untuk scaling

### File Management
- **multer** - File upload handling
- **sharp** - Image processing

### Email & Notifications
- **nodemailer** - Email sending
- **Firebase Admin SDK** - Push notifications
- **node-schedule** - Job scheduling

### Validation & Error Handling
- **zod** - Schema validation
- **express-async-errors** - Async error handling

---

## 🎨 Design System

### Colors
```
Primary: #2ec4b6 (Teal)
Secondary: #1a1a2e (Dark Navy)
Success: #10b981
Warning: #f59e0b
Error: #ef4444
Light: #f3f4f6
Dark: #111827
```

### Typography
- **Font Family**: Sharp Sans
- **Heading 1**: 32px, Bold
- **Heading 2**: 24px, Bold
- **Heading 3**: 18px, Semi-bold
- **Body**: 14px, Regular
- **Small**: 12px, Regular

### Responsive Breakpoints
```
Mobile: < 640px
Tablet: 640px - 1024px
Desktop: > 1024px
```

---

## 📦 DevOps & Deployment

### Version Control
- **Git** - Source control
- **GitHub** - Repository hosting

### CI/CD
- **GitHub Actions** - Continuous integration
- **Docker** - Containerization (optional)

### Hosting Options
- **Vercel** - Frontend deployment
- **Railway/Render** - Backend deployment
- **AWS/DigitalOcean** - Scalable hosting

### Monitoring & Analytics
- **Sentry** - Error tracking
- **Google Analytics** - Web analytics

---

## 🔐 Security Features

### Authentication
- JWT-based authentication
- Refresh token rotation
- Secure password hashing (bcrypt)

### Authorization
- Role-based access control (RBAC)
- Middleware for permission checking
- Resource-level authorization

### Data Protection
- HTTPS only (in production)
- CORS configuration
- CSRF protection
- Input validation & sanitization
- SQL injection prevention (via Prisma)
- XSS protection

---

**Last Updated**: 2026-06-11