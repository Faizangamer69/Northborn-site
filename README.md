# 🎸 Northborn - Band Website

> A modern, responsive website for the symphonic melodic death metal band Northborn, built with cutting-edge web technologies.

[![Next.js](https://img.shields.io/badge/Next.js-15.5.4-black.svg)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.1.0-blue.svg)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue.svg)](https://www.typescriptlang.org/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.x-38B2AC.svg)](https://tailwindcss.com/)
[![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED.svg)](https://www.docker.com/)

## 🚀 Overview

This project is a full-stack web application designed for the symphonic melodic death metal band Northborn. It demonstrates modern web development practices, containerization, and deployment strategies suitable for professional music industry websites.

## 🛠️ Tech Stack

### Frontend
- **Next.js 15.5.4** - React framework with App Router and Turbopack
- **React 19.1.0** - Latest React with concurrent features
- **TypeScript** - Type-safe development
- **TailwindCSS 4.x** - Utility-first CSS framework
- **ESLint** - Code quality and consistency

### Backend & Infrastructure
- **Docker** - Containerized deployment
- **MySQL 8.0** - Database management
- **WordPress** - Content management system
- **phpMyAdmin** - Database administration
- **Docker Compose** - Multi-container orchestration

## ✨ Features

- 🎨 **Modern Design** - Clean, responsive UI optimized for music industry standards
- ⚡ **Performance Optimized** - Built with Next.js Turbopack for lightning-fast builds
- 📱 **Mobile Responsive** - Seamless experience across all devices
- 🐳 **Containerized** - Docker-based deployment for consistency across environments
- 🔧 **Type Safety** - Full TypeScript implementation
- 🎵 **Music-Focused** - Tailored specifically for band/artist websites

## 🏗️ Architecture

```
📁 Northborn-site/
├── 📁 frontend/          # Next.js application
│   ├── 📁 src/app/       # App Router structure
│   ├── 📁 public/        # Static assets
│   ├── Dockerfile        # Frontend containerization
│   ├── next.config.ts    # Next.js configuration with standalone output
│   └── package.json      # Dependencies & scripts
├── docker-compose.yaml   # Unified container orchestration
├── .env                  # Environment variables
├── .env.example          # Environment template
└── README.md
```

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose
- Git
- (Optional) Node.js 20+ for local development

### Docker Deployment (Recommended)

1. **Clone the repository**
   ```bash
   git clone https://github.com/felicianorman/Northborn-site.git
   cd Northborn-site
   ```

2. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your database credentials
   ```

3. **Start the entire stack**
   ```bash
   docker-compose up --build
   ```

4. **Access your applications**
   - **Frontend**: http://localhost:3000
   - **WordPress Admin**: http://localhost:8080/wp-admin
   - **WordPress API**: http://localhost:8080/wp-json/wp/v2
   - **phpMyAdmin**: http://localhost:8081

### Local Development (Alternative)

1. **Install frontend dependencies**
   ```bash
   cd frontend
   npm install
   ```

2. **Start development server**
   ```bash
   npm run dev
   ```

### Available Scripts

- `npm run dev` - Start development server with Turbopack
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## 🌐 Deployment

### Docker Services
The application consists of 4 containerized services:

| Service | Port | Description |
|---------|------|-------------|
| **Frontend** | 3000 | Next.js application with standalone server |
| **WordPress** | 8080 | Headless CMS with REST API |
| **MySQL** | 3306 | Database (internal network only) |
| **phpMyAdmin** | 8081 | Database administration interface |

### Deployment Options
- **Local Development**: `docker-compose up --build`
- **Production**: Cloud platforms (AWS, DigitalOcean, etc.)
- **CI/CD**: Ready for automated deployment pipelines

### Docker Features
- ✅ **Multi-stage builds** for optimized production images
- ✅ **Standalone Next.js output** for minimal container size
- ✅ **Automatic service dependencies** and health checks
- ✅ **Persistent data volumes** for database and WordPress files
- ✅ **Internal networking** for secure service communication

## 💡 Key Development Highlights

- **Modern React**: Utilizes React 19's latest features and concurrent rendering
- **Performance First**: Turbopack integration for faster development builds
- **Type Safety**: Comprehensive TypeScript implementation
- **Containerization**: Production-ready Docker setup
- **Scalable Architecture**: Clean separation of concerns and modular structure

## 🔧 Environment Configuration

Create environment files for different deployment stages:

```env
# Database Configuration
MYSQL_ROOT_PASSWORD=your_password
MYSQL_DATABASE=northborn_db
MYSQL_USER=northborn_user
MYSQL_PASSWORD=user_password

# WordPress Configuration
WORDPRESS_DB_HOST=db:3306
WORDPRESS_DB_NAME=northborn_db
WORDPRESS_DB_USER=northborn_user
WORDPRESS_DB_PASSWORD=user_password
```

## 📈 Performance & SEO

- ✅ Server-side rendering with Next.js
- ✅ Image optimization
- ✅ Code splitting and lazy loading
- ✅ SEO-friendly structure
- ✅ Lighthouse score optimization

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Developer

**Felicia Norman**
- GitHub: [@felicianorman](https://github.com/felicianorman)
- LinkedIn: [Connect with me](https://www.linkedin.com/in/felicia-norman)

---

*This project showcases modern web development practices including React 19, Next.js 15, TypeScript, Docker containerization, and responsive design principles.*
