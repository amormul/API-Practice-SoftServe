# 🎬 Cinema System API

<p align="center">
  <img src="https://img.shields.io/badge/PHP-98.1%25-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP">
  <img src="https://img.shields.io/badge/HTML-1.1%25-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML">
  <img src="https://img.shields.io/badge/JavaScript-0.8%25-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/API-RESTful-009688?style=flat-square&logo=fastapi&logoColor=white" alt="RESTful">
  <img src="https://img.shields.io/badge/SoftServe-Practice-FF6B00?style=flat-square" alt="SoftServe">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square" alt="Status">
</p>

## 📋 Overview

**Cinema System API** is a comprehensive RESTful API developed as part of the SoftServe practice program. The API serves as the backend for a cinema management system, allowing users to browse movies, check session availability, and book seats. Built primarily with PHP, it provides a robust foundation for cinema applications.

## 🚀 Features

### 🎞️ Movie Management
- **List Movies**: Get a paginated list of all available movies
- **Movie Details**: Retrieve comprehensive information about specific movies
- **Search & Filter**: Find movies by title, genre, release date, or rating
- **Categories**: Browse movies by categories and collections

### 🗓️ Session Management
- **Available Sessions**: List all upcoming movie sessions
- **Session Details**: Get detailed information about specific sessions
- **Schedule**: Browse sessions by date, time, and cinema hall
- **Seat Layout**: Retrieve the layout and availability of seats for each session

### 🎫 Booking System
- **Seat Reservation**: Reserve seats for a specific movie session
- **Booking Confirmation**: Complete the booking process
- **Booking History**: Retrieve user's past bookings
- **Ticket Generation**: Generate digital tickets for confirmed bookings

### 👤 User Management
- **Authentication**: Secure login and registration system
- **User Profiles**: Manage user information and preferences
- **Role-Based Access**: Different permission levels for regular users and administrators

## 🛠️ Technology Stack

- **Backend**: PHP 8.0+
- **Database**: MySQL/MariaDB
- **API Architecture**: RESTful design principles
- **Authentication**: JWT (JSON Web Tokens)
- **Documentation**: OpenAPI/Swagger
- **Testing**: PHPUnit

## 📚 API Documentation

The API is fully documented using OpenAPI/Swagger specifications. Access the interactive documentation at:

```
/api/docs
```

### Example Endpoints

```
# Movies
GET    /api/movies                 # List all movies
GET    /api/movies/{id}            # Get movie details
GET    /api/movies/search?q={term} # Search for movies

# Sessions
GET    /api/sessions               # List all sessions
GET    /api/sessions/{id}          # Get session details
GET    /api/sessions/movie/{id}    # Get sessions for a specific movie

# Bookings
POST   /api/bookings               # Create a new booking
GET    /api/bookings/{id}          # Get booking details
GET    /api/bookings/user/{id}     # Get user's bookings
DELETE /api/bookings/{id}          # Cancel booking

# Authentication
POST   /api/auth/register          # Register new user
POST   /api/auth/login             # Login user
POST   /api/auth/refresh           # Refresh access token
```

## 🚀 Getting Started

### Prerequisites
- PHP 8.0 or higher
- Composer
- MySQL/MariaDB database
- Web server (Apache/Nginx)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/amormul/API-Practice-SoftServe.git
   cd API-Practice-SoftServe
   ```

2. **Install dependencies**
   ```bash
   composer install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit the .env file with your database credentials and other configuration
   ```

4. **Set up the database**
   ```bash
   php artisan migrate
   php artisan db:seed   # Optional: Populate with sample data
   ```

5. **Start the development server**
   ```bash
   php -S localhost:8000 -t public
   ```

6. **Access the API**
   ```
   Open http://localhost:8000/api in your browser or API client
   ```

## 🔧 Configuration

The API can be configured through the `.env` file:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=cinema_api
DB_USERNAME=root
DB_PASSWORD=

JWT_SECRET=your_jwt_secret_key
JWT_TTL=60  # Token time-to-live in minutes

PAGINATION_LIMIT=15
```

## 📁 Project Structure

```
src/
├── Controllers/        # API endpoint controllers
├── Models/             # Data models and database interactions
├── Middleware/         # Request middleware components
├── Services/           # Business logic services
├── Repositories/       # Data access layer
├── Routes/             # API route definitions
├── Helpers/            # Utility functions and helpers
├── Config/             # Configuration files
├── Database/
│   ├── Migrations/     # Database structure migrations
│   └── Seeders/        # Sample data seeders
└── Tests/              # API endpoint tests
```

## 🧪 Testing

Run the automated tests with:

```bash
composer test
```

Or for more detailed output:

```bash
vendor/bin/phpunit --testdox
```

## 🔒 Security

This API implements several security best practices:

- JWT-based authentication
- Input validation and sanitization
- CORS policy configuration
- Rate limiting
- SQL injection prevention
- XSS protection

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📖 Learning Resources

- [RESTful API Best Practices](https://restfulapi.net/)
- [PHP Official Documentation](https://www.php.net/docs.php)
- [SoftServe Academy](https://career.softserveinc.com/en-us/technology-education)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👏 Acknowledgments

- SoftServe mentors and instructors for their guidance and support
- All contributors who helped improve this API
- Open-source community for providing excellent tools and libraries

---

<p align="center">
  <i>Developed with ❤️ by <a href="https://github.com/amormul">amormul</a> — Last updated: June 8, 2025</i>
</p>
