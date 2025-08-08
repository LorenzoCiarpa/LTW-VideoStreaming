# 🎬 LTWIX - Netflix Clone

A university project recreating Netflix's interface and core functionalities using **vanilla JavaScript**, **PHP**, and **MySQL**. This web application demonstrates full-stack development skills without modern frameworks, showcasing traditional web development techniques and database management.

> **🎓 Academic Project**: Developed as part of a university web development course, focusing on fundamental web technologies and database integration.

## 📋 Project Overview

LTWIX is a Netflix-inspired streaming platform that replicates the visual design and essential features of the popular video streaming service. The project emphasizes **vanilla web technologies** and **server-side development** using PHP and MySQL.

### ✨ Key Features

- **🔐 User Authentication System**
  - User registration and login
  - Session management with cookies and session storage
  - Password change functionality
  - Forgot password feature

- **🎥 Video Streaming Platform**
  - Video player with custom controls
  - Resume watching functionality
  - Video progress tracking
  - Multiple video categories

- **📚 Content Management**
  - Film catalog with detailed information
  - Actor and director information
  - Category-based filtering
  - Search functionality

- **❤️ Personal Features**
  - Favorites list management
  - "Continue Watching" section
  - "Watch Again" recommendations
  - Personalized content suggestions

- **🎯 Recommendation System**
  - Content recommendations based on viewing history
  - Related content suggestions
  - Category-based recommendations

## 🛠️ Tech Stack

### Frontend
- **HTML5** - Semantic markup and structure
- **CSS3** - Styling, animations, and responsive design
- **Vanilla JavaScript** - Client-side functionality and DOM manipulation
- **jQuery** - AJAX requests and simplified DOM operations

### Backend
- **PHP** - Server-side logic and API endpoints
- **MySQL** - Database management and data persistence

### Architecture
- **MVC Pattern** - Separation of concerns with dedicated files for:
  - Models (`php/query_functions.php`)
  - Controllers (`php/query.php`, `php/login.php`, etc.)
  - Views (`*.html` files)

## 📁 Project Structure

```
LTWIX/
├── 📄 Frontend Pages
│   ├── index.html          # Main dashboard
│   ├── login.html          # User login
│   ├── sign_up.html        # User registration
│   ├── vid.html            # Video player
│   ├── change_password.html # Password management
│   └── forgot_password.html # Password recovery
│
├── 🎨 Assets
│   ├── style/              # CSS stylesheets
│   ├── script/             # JavaScript files
│   ├── images/             # Movie posters and UI images
│   └── Media/              # Video files
│
├── ⚙️ Backend
│   ├── php/
│   │   ├── connection.php      # Database connection
│   │   ├── query_functions.php # Database operations
│   │   ├── query.php          # API endpoints
│   │   ├── login.php          # Authentication logic
│   │   └── sign_up.php        # Registration logic
│   │
└── 🗄️ Database
    └── database/
        └── netflix.sql        # Database schema and sample data
```

## 🎯 Core Functionalities

### 🔐 Authentication System
- **Registration**: New user account creation with email validation
- **Login**: Secure user authentication with session management
- **Password Management**: Change and reset password functionality
- **Session Handling**: Cookie-based and session storage authentication

### 🎬 Video Management
- **Streaming**: HTML5 video player with custom controls
- **Progress Tracking**: Resume videos from where you left off
- **Categories**: Browse content by genre (Action, Comedy, Sci-Fi, Horror, etc.)
- **Search**: Find movies by title

### 👤 User Experience
- **Personal Library**: Add/remove movies from favorites
- **Viewing History**: Track watched content
- **Recommendations**: Suggest related content based on actors and categories
- **Responsive Design**: Mobile-friendly interface

## 🗄️ Database Schema

The application uses a well-structured MySQL database with the following main tables:

- **`utente`** - User accounts and authentication
- **`film`** - Movie catalog with metadata
- **`attore`** - Actor information
- **`regista`** - Director information
- **`cast`** - Movie cast relationships
- **`preferito`** - User favorites tracking

## 🚀 Getting Started

### Prerequisites
- **Web Server** (Apache/Nginx)
- **PHP 7.4+**
- **MySQL 5.7+**
- **Web Browser** (Chrome, Firefox, Safari)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/LorenzoCiarpa/LTW-VideoStreaming.git
   cd LTW-VideoStreaming
   ```

2. **Set up the database**
   ```bash
   # Import the database schema
   mysql -u your_username -p < database/netflix.sql
   ```

3. **Configure database connection**
   ```php
   // Edit php/connection.php with your database credentials
   $servername = "localhost";
   $username = "your_username";
   $password = "your_password";
   $dbname = "netflix";
   ```

4. **Deploy to web server**
   - Copy all files to your web server directory
   - Ensure PHP has read/write permissions
   - Configure virtual host if necessary

5. **Access the application**
   ```
   http://localhost/LTW-VideoStreaming
   ```

### Demo Credentials
```
Email: prova@prova.it
Password: prova123
```

## 🎨 Features Showcase

### 🏠 Homepage
- Netflix-style carousel slider
- Featured content sections
- Category navigation
- User menu with profile options

### 🎥 Video Player
- Custom HTML5 video controls
- Full-screen support
- Progress saving and resume functionality
- Responsive video scaling

### 📱 Responsive Design
- Mobile-optimized interface
- Touch-friendly navigation
- Adaptive layout for different screen sizes

## 🔧 API Endpoints

The application provides several PHP endpoints for data management:

- **Authentication**
  - `POST /php/login.php` - User login
  - `POST /php/sign_up.php` - User registration
  - `POST /php/change_password.php` - Password change

- **Content Management**
  - `GET /php/query.php?command=getFilm` - Get movie details
  - `GET /php/query.php?command=getCategory` - Get movies by category
  - `GET /php/query.php?command=getCast` - Get movie cast

- **User Features**
  - `POST /php/query.php?command=addPreferiti` - Add to favorites
  - `GET /php/query.php?command=getPreferiti` - Get user favorites
  - `POST /php/query.php?command=updateTime` - Update viewing progress

## 📄 License

This project is created for educational purposes. All rights reserved.

## 👨‍💻 Author

**Lorenzo Ciarpa**
- GitHub: [@LorenzoCiarpa](https://github.com/LorenzoCiarpa)
- Project: [LTW-VideoStreaming](https://github.com/LorenzoCiarpa/LTW-VideoStreaming)

---

*🎬 Experience the nostalgia of traditional web development while building modern streaming experiences!*
