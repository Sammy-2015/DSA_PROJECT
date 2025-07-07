
# Mentorship Matching Platform

A comprehensive full-stack web application built for incubators and accelerators to connect mentors with mentees. Features role-based access control, session booking, and comprehensive mentorship management.

## 🚀 Features

### ✅ Authentication & Authorization
- **JWT-based authentication** with secure HTTP-only cookies
- **Role-based access control** (Admin, Mentor, Mentee)
- **Protected routes** with automatic redirects
- **Password hashing** with bcrypt for security

### ✅ User Management
- **Three distinct user roles** with different permissions
- **User profiles** with skills, goals, and bio information
- **Profile editing** and management functionality
- **Admin role assignment** capabilities

### ✅ Mentorship System
- **Mentor discovery** with filtering by skills and industry
- **Mentorship request system** (pending, accepted, rejected)
- **Session booking** with time slot management
- **Feedback system** with ratings and comments

### ✅ Admin Features
- **User management dashboard** with role assignments
- **Match oversight** and manual assignment capabilities
- **Session monitoring** and analytics
- **Platform statistics** and metrics

### ✅ Technical Implementation
- **RESTful API** with proper HTTP methods and status codes
- **Input validation** using Zod schemas
- **Error handling** with graceful error states
- **Responsive design** that works on all screen sizes
- **Clean code structure** with modular components

## 🧪 Test Credentials

Use these credentials to test different user roles:

### Admin Account
- **Email:** admin@mentormatch.com
- **Password:** admin123

### Mentor Account
- **Email:** sarah.chen@email.com
- **Password:** mentor123

### Mentee Account
- **Email:** alex.jones@email.com
- **Password:** mentee123

## 🛠️ Technology Stack

### Frontend
- **React** with TypeScript
- **Tailwind CSS** with shadcn/ui components
- **TanStack Query** for server state management
- **React Hook Form** with Zod validation
- **Wouter** for client-side routing

### Backend
- **Express.js** with TypeScript
- **PostgreSQL** with Drizzle ORM
- **JWT** for authentication
- **bcrypt** for password hashing
- **Zod** for input validation

### Database
- **PostgreSQL** via Neon serverless
- **Connection pooling** for performance
- **Automated migrations** with Drizzle Kit

## 📡 API Endpoints

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/me` - Get current user

### Users & Profiles
- `GET /api/users/me` - Get current user with profile
- `PUT /api/users/me/profile` - Update user profile

### Mentors
- `GET /api/mentors` - Get all mentors
- `GET /api/mentors/:id/availability` - Get mentor availability
- `POST /api/mentors/availability` - Create availability slot
- `PUT /api/mentors/availability/:id` - Update availability slot
- `DELETE /api/mentors/availability/:id` - Delete availability slot

### Mentorship Requests
- `POST /api/requests` - Create mentorship request
- `GET /api/requests/sent` - Get sent requests (mentee)
- `GET /api/requests/received` - Get received requests (mentor)
- `PUT /api/requests/:id` - Update request status

### Sessions
- `POST /api/sessions` - Create session
- `GET /api/sessions/mentor` - Get mentor sessions
- `GET /api/sessions/mentee` - Get mentee sessions
- `PUT /api/sessions/:id/feedback` - Submit session feedback

### Admin
- `GET /api/admin/stats` - Get platform statistics
- `GET /api/admin/users` - Get all users
- `PUT /api/admin/users/:id/role` - Update user role
- `GET /api/admin/sessions` - Get all sessions

## 🗄️ Database Schema

### Users
- User authentication and basic information
- Role-based permissions (admin, mentor, mentee)

### User Profiles
- Extended user information (bio, skills, goals)
- Industry and expertise areas

### Mentor Availability
- Time slots when mentors are available
- Day of week and time ranges

### Mentorship Requests
- Requests from mentees to mentors
- Status tracking (pending, accepted, rejected)

### Mentorship Sessions
- Scheduled sessions between mentors and mentees
- Session topics and notes

### Session Feedback
- Post-session ratings and comments
- Performance tracking and improvement

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd mentorship-platform
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   - Create a `.env` file in the root directory
   - Add your database URL and JWT secret
   ```env
   DATABASE_URL=your_neon_database_url
   JWT_SECRET=your_jwt_secret_key
   ```

4. **Push database schema**
   ```bash
   npm run db:push
   ```

5. **Start the development server**
   ```bash
   npm run dev
   ```

6. **Access the application**
   - Open your browser and navigate to `http://localhost:5000`
   - Use the test credentials above to explore different user roles

## 👥 User Roles & Permissions

### Admin
- View all users and their profiles
- Assign and change user roles
- Monitor all sessions and matches
- Access platform statistics

### Mentor
- Set availability schedules
- View and respond to mentorship requests
- Manage scheduled sessions
- Provide session feedback

### Mentee
- Browse and search mentors
- Send mentorship requests
- Book sessions with accepted mentors
- Provide session feedback

## 🔒 Security Features

- **JWT Authentication** with HTTP-only cookies
- **Password hashing** with bcrypt
- **Role-based route protection**
- **Input validation** on all forms
- **SQL injection protection** via Drizzle ORM
- **Secure session management**

## 📁 Project Structure

```
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Page components by role
│   │   ├── hooks/          # Custom React hooks
│   │   └── lib/            # Utility functions
├── server/                 # Express backend
│   ├── auth.ts             # Authentication logic
│   ├── db.ts               # Database connection
│   ├── routes.ts           # API routes
│   └── storage.ts          # Data access layer
├── shared/                 # Shared schemas and types
└── README.md               # This file
```

## 🧑‍💻 Development

The application uses modern development practices:
- **TypeScript** for type safety
- **Zod schemas** for validation
- **Drizzle ORM** for database operations
- **React Query** for state management
- **Modular architecture** for maintainability

## 🚀 Deployment

The application is configured for deployment on Replit:
- Automatic dependency installation
- Environment variable management
- Production build optimization
- Database migrations on deploy

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License.

## 🎯 Future Enhancements

- [ ] Email notifications for session reminders
- [ ] Video call integration
- [ ] Advanced matching algorithms
- [ ] Mobile app development
- [ ] Analytics dashboard
- [ ] Bulk user import
- [ ] Calendar integration

## 📞 Support

For questions or issues, please open an issue in the repository or contact the development team.

---

Built with ❤️ for the mentorship community

