 AlWay Download
AlWay Download is a modern, browser-based universal direct downloader and public media search platform built with PHP, MySQL, JavaScript, AJAX, HTML, and CSS

It provides users with a simple interface to search for downloadable content, generate direct download links, manage download history, and access their personal account from both desktop and mobile devices.

🚀 Features

* 🔎 Universal public media/file search
* ⬇️ Direct download support
* 🎬 YouTube/media downloading through `yt-dlp`
* 🔗 Direct URL processing
* 📥 Download history
* 👤 User registration and login
* 🔐 Session-based authentication
* 📊 Personal user dashboard
* 📱 Mobile-friendly responsive interface
* 🖥️ Desktop-friendly UI
* ⚡ AJAX-based API requests
* 🔔 Toast notifications
* 🎨 Modern dark/glassmorphism-style interface
* 🖼️ Custom logo and user avatar support
* 🗂️ Download metadata and file information
* 🛠️ PHP/MySQL backend

## 🧰 Technology Stack

### Frontend

* HTML5
* CSS3
* JavaScript
* AJAX
* Fetch API
* Responsive UI

### Backend

* PHP
* MySQL / MariaDB
* PDO
* PHP Sessions
* REST-style PHP API endpoints

### Download Engine

* `yt-dlp`

## 📁 Project Structure

```text
Alwasys_download/
│
├── api/
│   ├── auth.php
│   ├── direct_url.php
│   ├── download_stream.php
│   ├── history.php
│   ├── search.php
│   ├── search_backup.php
│   └── suggest.php
│
├── assets/
│   ├── css/
│   │   └── style.css
│   │
│   ├── images/
│   │   ├── default_avatar.svg
│   │   └── logo.svg
│   │
│   └── js/
│       ├── app.js
│       ├── auth.js
│       └── toast.js
│
├── bin/
│   └── yt-dlp.exe
│
├── config/
│   ├── db.php
│   └── setup.sql
│
├── dashboard.php
├── index.php
├── login.php
├── logout.php
├── register.php
└── .htaccess
```

## 🔐 User Authentication

AlWay Download includes a complete account system.

Users can:

* Create an account
* Sign in using email/password
* Sign out securely
* Access their personal dashboard
* View account information
* View download statistics
* View recent download history

### Registration Fields

The registration system supports:

```text
Full Name
Mobile Number
Gmail / Email
Password
```

Passwords are processed through the application's authentication system rather than being stored as plain text.

## 📥 Download History

Authenticated users can access their download history.

The system records information such as:

* File name
* Category
* File type
* File size
* Download URL
* Download date/time

The dashboard also provides a total download count for the user.

## 🔎 Search System

The application contains API endpoints for searching and suggesting downloadable content.

Main endpoints include:

```text
api/search.php
api/search_backup.php
api/suggest.php
```

The frontend communicates with these APIs asynchronously using JavaScript/AJAX.

## 🔗 Direct URL Downloader

The project includes a dedicated direct URL processing API:

```text
api/direct_url.php
```

This allows the application to process supported direct media/download URLs and prepare downloadable resources.

## 🎬 yt-dlp Integration

The project includes:

```text
bin/yt-dlp.exe
```

`yt-dlp` is used as the media download engine for supported platforms.

The application communicates with the downloader through its PHP backend rather than requiring users to manually install the command-line tool.

## ⚡ Download Streaming

The project contains:

```text
api/download_stream.php
```

This endpoint is responsible for handling download/streaming operations between the user and the requested resource.

## 🗄️ Database

Database configuration is located at:

```text
config/db.php
```

The initial database structure is provided through:

```text
config/setup.sql
```

The database stores application data such as user accounts and download history.

## 🖥️ User Dashboard

After authentication, users can access:

```text
dashboard.php
```

The dashboard provides:

* User profile
* Avatar
* Email
* Mobile number
* Verification/member information
* Total downloads
* Authentication information
* Download history

## 🎨 User Interface

AlWay Download uses a modern dark interface with:

* Glass-style cards
* Responsive layouts
* Ambient background effects
* Gradient branding
* Modern buttons
* Category tabs
* Toast notifications
* Responsive navigation
* Mobile support

The primary frontend styling is contained in:

```text
assets/css/style.css
```

## ⚙️ Installation

### Requirements

Before running the project, install:

* Windows
* XAMPP or another PHP environment
* Apache
* PHP
* MySQL / MariaDB
* Modern web browser

### Setup

1. Clone or download the repository.

2. Place the project inside your web server directory.

For XAMPP:

```text
C:\xampp\htdocs\Alwasys_download
```

3. Start:

```text
Apache
MySQL
```

from the XAMPP Control Panel.

4. Create/import the database using:

```text
config/setup.sql
```

5. Configure your database credentials inside:

```text
config/db.php
```

6. Open the application in your browser:

```text
http://localhost/Alwasys_download/
```

## 🔧 Configuration

Database settings should be configured according to your local environment.

Typical configuration values include:

```text
Database Host
Database Name
Database Username
Database Password
```

Do not publish production database credentials to GitHub.

## 📱 Responsive Design

The interface is designed to work across:

* Desktop
* Laptop
* Tablet
* Mobile

The responsive layout automatically adapts navigation, cards, search components, and dashboard elements to smaller screens.

## 🔒 Security Considerations

This project is intended for development and controlled deployment.

Before deploying publicly, additional security measures should be implemented, including:

* CSRF protection
* Strong session configuration
* Rate limiting
* Input validation
* URL validation
* File download restrictions
* Secure command execution
* Process/resource limits
* Authentication hardening
* Production database credentials
* HTTPS
* Abuse prevention

Because the application handles external URLs and invokes a download engine, **never expose unrestricted command execution or downloader functionality to untrusted users without proper validation and isolation**.

## 🛠️ Main API Components

| API                   | Purpose                               |
| --------------------- | ------------------------------------- |
| `auth.php`            | Authentication and account operations |
| `search.php`          | Search functionality                  |
| `search_backup.php`   | Backup search functionality           |
| `suggest.php`         | Search suggestions                    |
| `direct_url.php`      | Direct URL processing                 |
| `download_stream.php` | Download/stream handling              |
| `history.php`         | User download history                 |

## 📌 Project Status

**Active Development**

AlWay Download currently provides the foundation for a universal downloader platform with authentication, search, direct URL processing, download history, user dashboards, and `yt-dlp` integration.

## 🔮 Future Improvements

Possible future features include:

* Google/Gmail OAuth authentication
* More supported download platforms
* Download format selection
* Video quality selection
* Audio-only downloads
* Download queue
* Download progress tracking
* Advanced search filters
* Favorites/bookmarks
* Admin dashboard
* User management
* Download analytics
* API rate limiting
* Cloud storage integration
* Docker deployment
* Background download workers
* Improved security sandboxing
* Automatic metadata extraction

## 📄 License

Choose and add an appropriate license before publishing the repository publicly.

For example:

```text
MIT License
```

## 👨‍💻 Author

ARK ALI RAZA KHASKHELI 

AlWay Download is a web development project focused on building a unified, easy-to-use direct downloading and media search platform.
