# 🚀 Ahmed Essam Ahmed - Full Stack Developer Portfolio

A modern, dynamic portfolio website built with Next.js 15, React 19, and Prisma ORM. Features a powerful admin dashboard for content management and a beautiful, responsive frontend.

![Next.js](https://img.shields.io/badge/Next.js-15.5.6-black?style=for-the-badge&logo=next.js)
![React](https://img.shields.io/badge/React-19.1.0-61DAFB?style=for-the-badge&logo=react)
![Prisma](https://img.shields.io/badge/Prisma-6.1.0-2D3748?style=for-the-badge&logo=prisma)
![TailwindCSS](https://img.shields.io/badge/Tailwind-3.4.1-38B2AC?style=for-the-badge&logo=tailwind-css)

## ✨ Features

### Frontend
- 🎨 **Modern UI/UX** - Clean, responsive design with smooth animations
- 📱 **Fully Responsive** - Optimized for all screen sizes
- ⚡ **Dynamic Content** - All sections powered by API endpoints
- 🖼️ **Image Support** - Upload images or use URLs for projects
- 🎯 **Sections**:
  - Hero with social links
  - About Me
  - Work Experience with technologies
  - Projects (Featured & Other)
  - Skills by categories
  - Education & Achievements
  - Contact Information
  - Contact Form

### Admin Dashboard
- 🔐 **Secure Authentication** - JWT-based auth with HTTP-only cookies
- 📊 **Full CRUD Operations** - Manage all content sections
- 🖼️ **Image Management** - Upload files or use external URLs
- 👤 **Account Settings** - Change password functionality
- 📧 **Contact Form Management** - View and respond to submissions
- 🎛️ **Sections Management**:
  - Hero Section
  - About Section
  - Experience (with technologies)
  - Projects (with technologies and images)
  - Skills (categorized)
  - Education (with achievements)
  - Contact Info & Methods

## 🛠️ Tech Stack

### Frontend
- **Next.js 15.5.6** - React framework with App Router
- **React 19.1.0** - UI library
- **TailwindCSS 3.4.1** - Utility-first CSS
- **Bebas Neue & Manrope** - Custom fonts

### Backend
- **Next.js API Routes** - Serverless API endpoints
- **Prisma ORM 6.1.0** - Database toolkit
- **SQLite** - Database (easily switchable to PostgreSQL/MySQL)
- **JWT** - Authentication tokens
- **bcryptjs** - Password hashing

### Tools & Utilities
- **pnpm** - Fast package manager
- **ESLint** - Code linting
- **PostCSS** - CSS processing

## 📦 Installation

### Prerequisites
- Node.js 18+ installed
- pnpm installed (or use npm/yarn)

### Setup Steps

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/portfolio.git
cd portfolio
```

2. **Install dependencies**
```bash
pnpm install
```

3. **Set up environment variables**
Create a `.env` file in the root directory:
```env
DATABASE_URL="file:./dev.db"
JWT_SECRET="your-super-secret-jwt-key-change-this-in-production"
```

4. **Initialize the database**
```bash
npx prisma generate
npx prisma db push
node prisma/seed.js
```

5. **Run the development server**
```bash
pnpm dev
```

6. **Open your browser**
- Portfolio: [http://localhost:3000](http://localhost:3000)
- Admin Dashboard: [http://localhost:3000/admin/login](http://localhost:3000/admin/login)

### Default Admin Credentials
```
Email: ahmeddev@esan.com
Password: ahmedesam317123D
```
⚠️ **Change these credentials immediately after first login!**

## 📁 Project Structure

```
portfolio/
├── prisma/
│   ├── schema.prisma      # Database schema
│   └── seed.js            # Database seed data
├── public/
│   ├── uploads/           # Uploaded images
│   ├── projects/          # Project images
│   ├── icons/             # Icon files
│   └── CV.pdf             # Resume file
├── src/
│   ├── app/
│   │   ├── api/           # API routes
│   │   │   ├── about/
│   │   │   ├── admin/
│   │   │   ├── contact/
│   │   │   ├── education/
│   │   │   ├── experience/
│   │   │   ├── hero/
│   │   │   ├── projects/
│   │   │   ├── skills/
│   │   │   └── upload/
│   │   ├── admin/         # Admin dashboard pages
│   │   │   ├── dashboard/
│   │   │   ├── login/
│   │   │   ├── hero/
│   │   │   ├── about/
│   │   │   ├── experience/
│   │   │   ├── projects/
│   │   │   ├── skills/
│   │   │   ├── education/
│   │   │   ├── contact/
│   │   │   └── settings/
│   │   ├── components/    # Frontend components
│   │   │   ├── Hero/
│   │   │   ├── About/
│   │   │   ├── Experience/
│   │   │   ├── Projects/
│   │   │   ├── Skills/
│   │   │   ├── Education/
│   │   │   ├── Contact/
│   │   │   └── Footer/
│   │   ├── globals.css    # Global styles
│   │   ├── layout.js      # Root layout
│   │   └── page.js        # Home page
│   └── lib/
│       ├── auth.js        # JWT utilities
│       └── prisma.js      # Prisma client
├── .env                   # Environment variables
├── next.config.mjs        # Next.js configuration
├── tailwind.config.mjs    # Tailwind configuration
└── package.json           # Dependencies
```

## 🎨 Customization

### Update Personal Information
Edit `prisma/seed.js` with your information and run:
```bash
node prisma/seed.js
```

### Change Theme Colors
Edit `src/app/globals.css` and component styles in `src/app/components/`

### Add New Sections
1. Create Prisma model in `prisma/schema.prisma`
2. Create API route in `src/app/api/`
3. Create admin page in `src/app/admin/`
4. Create frontend component in `src/app/components/`
5. Add to home page in `src/app/page.js`

## 🚀 Deployment

### Vercel (Recommended)
1. Push code to GitHub
2. Import project in [Vercel](https://vercel.com)
3. Add environment variables
4. Deploy!

### Environment Variables for Production
```env
DATABASE_URL="your-production-database-url"
JWT_SECRET="strong-random-secret-key"
```

### Database Migration
For production, consider using PostgreSQL:
```env
DATABASE_URL="postgresql://user:password@host:5432/dbname"
```

Then run:
```bash
npx prisma generate
npx prisma db push
node prisma/seed.js
```

## 📝 API Documentation

### Public Endpoints
- `GET /api/hero` - Get hero section data
- `GET /api/about` - Get about section data
- `GET /api/experience` - Get all experiences
- `GET /api/projects` - Get all projects
- `GET /api/skills` - Get skills by categories
- `GET /api/education` - Get education records
- `GET /api/contact/info` - Get contact information
- `GET /api/contact/methods` - Get contact methods
- `POST /api/contact` - Submit contact form

### Admin Endpoints (Authentication Required)
- `POST /api/admin/auth/login` - Login
- `POST /api/admin/auth/logout` - Logout
- `POST /api/admin/change-password` - Change password
- `PUT /api/hero` - Update hero section
- `PUT /api/about` - Update about section
- CRUD operations for all sections...

## 🔒 Security Features

- ✅ JWT authentication with HTTP-only cookies
- ✅ Password hashing with bcryptjs
- ✅ Protected admin routes
- ✅ CORS configuration
- ✅ Input validation
- ✅ Secure file upload

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Ahmed Essam Ahmed**
- Email: ahmed.essam.m.dev@gmail.com
- Phone: +20 1200997915
- Location: Maadi, Cairo, Egypt
- LinkedIn: [Ahmed Essam](https://www.linkedin.com/in/ahmed-essam-630a33253/)
- GitHub: [ahmedessam3270](https://github.com/ahmedessam3270)

## 🙏 Acknowledgments

- Next.js team for the amazing framework
- Vercel for hosting
- Prisma for the excellent ORM
- TailwindCSS for utility classes

---

⭐ **If you like this project, please give it a star!** ⭐
