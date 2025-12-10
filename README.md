## Django Crud Operations with static and Media file

### Overview
This project demonstrates CRUD (Create, Read, Update, Delete) operations in Django with comprehensive static and media file handling.

### Features
- **CRUD Operations**: Full Create, Read, Update, and Delete functionality
- **Static File Management**: CSS, JavaScript, and image asset organization
- **Media Uploads**: User file upload and storage handling
- **Django ORM**: Database operations and model management
- **File Validation**: Input validation for uploads

### Prerequisites
- Python 3.8 or higher
- Django 3.0 or higher
- pip package manager
- Pillow library for image handling

### Project Structure
```
project-root/
├── app/
│   ├── models.py          # Database models
│   ├── views.py           # View logic
│   ├── urls.py            # URL routing
│   └── templates/
├── static/                # CSS, JS, images
├── media/                 # User uploads
├── manage.py
```

### Installation & Setup
1. **Clone the repository**
    ```bash
    git clone <repository-url>
    cd Django-advance-CRUD
    ```

2. **Install dependencies**
    ```bash
    pip install Pillow
    ```

3. **Configure database**
    ```bash
    python manage.py migrate
    ```

4. **Configure settings.py**
    ```python
    MEDIA_URL = '/media/'
    MEDIA_ROOT = 'media/'
    STATIC_URL = '/static/'
    STATICFILES_DIRS = ['static']
    ```

5. **Configure urls.py**
    ```python
    from django.conf import settings
    from django.conf.urls.static import static
    
    urlpatterns = [
        # Your URLs here
    ] + static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
    ```

6. **Start development server**
    ```bash
    python manage.py runserver
    ```



### Usage
1. Navigate to `http://localhost:8000`
2. Use the web interface to Create, Read, Update, and Delete records
3. Upload media files through designated forms
