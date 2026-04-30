# 📰 Blog CRUD Django

[![Django](https://img.shields.io/badge/Django-6.0.4-green.svg)](https://www.djangoproject.com/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A comprehensive Django-based blog application featuring full CRUD operations for articles, user authentication, and a clean, responsive interface. Perfect for learning Django or as a starting point for your own blog project.

## ✨ Features

- **📝 Article Management**: Create, read, update, and delete blog articles
- **🖼️ Image Uploads**: Support for article images with organized storage
- **👤 User Authentication**: Secure login and signup system
- **🎨 Responsive Design**: Clean, modern UI with Bootstrap styling
- **🔒 Author Attribution**: Articles linked to their authors
- **📅 Timestamps**: Automatic creation and update tracking
- **🛡️ Security**: CSRF protection and Django's built-in security features

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)
- Virtual environment (recommended)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/blog-crud-django.git
   cd blog-crud-django
   ```

2. **Create and activate virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create superuser (optional, for admin access)**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. **Open your browser**
   
   Navigate to [http://127.0.0.1:8000](http://127.0.0.1:8000)

## 📁 Project Structure

```
blog-crud-django/
├── base_project/           # Main Django project settings
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py         # Project configuration
│   ├── urls.py             # Main URL routing
│   └── wsgi.py
├── blog/                   # Blog application
│   ├── migrations/         # Database migrations
│   ├── __init__.py
│   ├── admin.py           # Django admin configuration
│   ├── apps.py
│   ├── models.py          # Article model
│   ├── tests.py
│   ├── urls.py            # Blog URL patterns
│   └── views.py           # Blog views
├── accounts/               # User accounts application
│   ├── migrations/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py          # (Uses Django's default User model)
│   ├── tests.py
│   ├── urls.py            # Authentication URLs
│   └── views.py           # Authentication views
├── articles_images/        # Uploaded article images
├── static/                 # Static files (CSS, JS, images)
│   └── css/
│       └── base.css
├── templates/              # HTML templates
│   ├── _base.html         # Base template
│   ├── articles_list.html # Article list page
│   ├── articles_detail.html # Article detail page
│   ├── article_create.html # Create article form
│   ├── article_update.html # Update article form
│   ├── article_delete.html # Delete confirmation
│   └── registration/
│       ├── login.html     # Login page
│       └── signup.html    # Signup page
├── db.sqlite3              # SQLite database
├── manage.py               # Django management script
└── requirements.txt        # Python dependencies
```

## 🛠️ Technologies Used

- **Backend**: Django 6.0.4
- **Database**: SQLite (development) / PostgreSQL (production recommended)
- **Frontend**: HTML5, CSS3, Bootstrap
- **Authentication**: Django's built-in auth system
- **File Uploads**: Django's file handling
- **Version Control**: Git

## 📖 Usage

### User Registration and Login

1. Visit the signup page to create an account
2. Login with your credentials
3. Access your dashboard to manage articles

### Managing Articles

- **View Articles**: Browse all published articles on the home page
- **Create Article**: Click "Create Article" to add new content with images
- **Edit Article**: Update your own articles (author-restricted)
- **Delete Article**: Remove articles with confirmation

### Admin Panel

Access `/admin/` with superuser credentials to manage users and articles.

## 🔧 Configuration

### Environment Variables

For production deployment, set these environment variables:

```bash
DEBUG=False
SECRET_KEY=your-secret-key-here
DATABASE_URL=your-database-url
ALLOWED_HOSTS=your-domain.com
```

### Static Files

For production, configure static file serving:

```python
# In settings.py
STATIC_ROOT = BASE_DIR / 'staticfiles'
STATIC_URL = '/static/'

# Run collectstatic
python manage.py collectstatic
```

## 🧪 Testing

Run the test suite:

```bash
python manage.py test
```

## 🚀 Deployment

### Heroku Deployment

1. Install Heroku CLI
2. Create Heroku app
3. Set environment variables
4. Deploy:

```bash
heroku create your-app-name
git push heroku main
heroku run python manage.py migrate
```

### Docker Deployment

Add a `Dockerfile` and `docker-compose.yml` for containerized deployment.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Django documentation and community
- Bootstrap for UI components
- All contributors and users

## 📞 Support

If you have any questions or issues, please open an issue on GitHub or contact the maintainers.

---

**Happy blogging! 🎉**