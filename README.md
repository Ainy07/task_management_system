# task_management_system
using django , drf
## Description

This project is a backend for a simple task management system built with Django and Django Rest Framework. The application includes Task and Label models, with CRUD operations and user authentication.

## Features

- Task model with title, description, completion status, owner, and a many-to-many relationship with Label.
- Label model with name and owner.
- API endpoints for CRUD operations on both Task and Label models.
- User authentication and authorization.
- Custom filters for listing tasks and labels related to the authenticated user.

## Setup Instructions

### Prerequisites

- Python 3.8+
- Django 3.2+
- Django Rest Framework 3.12+
- Git

### Installation

1. **Fork the Repository**

   Fork this repository to your GitHub account.

2. **Clone the Repository**

   ```bash
   git clone https://github.com/Ainy07/task_management_system_using_Django-drf
.git
   cd task_management_system_using_Django-drf


3. Create a Virtual Environment
```python -m venv venv```
source venv/bin/activate   # On Windows, use `venv\Scripts\activate`


4. Install Dependencies
```pip install -r requirements.txt```


## Configuration
1. Update settings.py

- Add tasks and rest_framework to the INSTALLED_APPS list in task_management/settings.py.
INSTALLED_APPS = [
    ...
    'rest_framework',
    'tasks',
]


## Database Setup
1. Apply Migrations

- python manage.py makemigrations
- python manage.py migrate

2. Create Superuser
 
- python manage.py createsuperuser

## Run the Server

- python manage.py runserver

### Testing
# Create Users
1. Create 2 users using the Django shell:
- python manage.py shell
```
from django.contrib.auth.models import User
User.objects.create_user('user1', password='password1', is_staff=True)
User.objects.create_user('user2', password='password2', is_staff=True)

```
```
from django.contrib.auth.models import User

# If you need to create a user:
user = User.objects.create_user('username', password='password')
user.is_staff = True
user.save()

# Fetch the user:
user = User.objects.get(username='username')  # Replace 'username' with your actual username
```
# Run Tests
- python manage.py test


## Testing CRUD Operations
1. Create a Task

Send a POST request to /api/tasks/ with the task details.

2. Read Tasks

Send a GET request to /api/tasks/ to list tasks.
Send a GET request to /api/tasks/<task_id>/ to retrieve a specific task.

3. Update a Task

Send a PUT request to /api/tasks/<task_id>/ with the updated task details.

4. Delete a Task

Send a DELETE request to /api/tasks/<task_id>/.

1. Create a Label

Send a POST request to /api/labels/ with the label details.

2. Read Labels

Send a GET request to /api/labels/ to list labels.
Send a GET request to /api/labels/<label_id>/ to retrieve a specific label.

3. Update a Label

Send a PUT request to /api/labels/<label_id>/ with the updated label details.

4. Delete a Label

Send a DELETE request to /api/labels/<label_id>/



## Challenge Details
Create 2 users with the is_staff flag set to True for admin site access.
# User credentials:
- User1: user1, Password: password1
- User2: user2, Password: password2


## Contributing
Please ensure your code adheres to the PEP 8 style guide and includes proper documentation. Commit your changes regularly with meaningful commit messages.

## License
This project is licensed under the MIT License.


This `README.md` provides a comprehensive guide for setting up and running the project, as well as contributing to it. 