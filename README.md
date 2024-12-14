# Project Title: Django Menu Items API

## Description
This project is a simple Django application that allows users to submit menu items via a web form. The submitted items are saved in a MySQL database, and the system provides real-time feedback on successful submissions using AJAX requests.

## Features
- **Form Submission**: Users can submit menu items with `item_name`, `category`, and `description` fields.
- **AJAX Integration**: Form submissions do not reload the page, providing a smooth user experience.
- **Data Persistence**: Submitted menu items are stored in a MySQL database.

## Prerequisites
Make sure you have the following installed on your local machine:
- **Python 3.13.0**
- **MySQL Database**
- **Django 4.1+**

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yousefmamdohfawzy/-form-with-JavaScript.git
   cd myproject
   ```

2. **Create a virtual environment**
   ```bash
   pipenv shell
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure the MySQL database**
   - Open `settings.py` and set your MySQL database credentials under the `DATABASES` section:
     ```python
     DATABASES = {
         'default': {
             'ENGINE': 'django.db.backends.mysql',
             'NAME': 'menu_items',
             'USER': 'root',
             'PASSWORD': 'yourpassword',
             'HOST': '127.0.0.1',
             'PORT': '3306',
         }
     }
     ```

5. **Apply migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

6. **Create a superuser** (optional, for admin access)
   ```bash
   python manage.py createsuperuser
   ```

7. **Run the development server**
   ```bash
   python manage.py runserver
   ```
   Open your browser and go to `http://127.0.0.1:8000/`.

## Usage
1. Navigate to `http://127.0.0.1:8000/` to see the form.
2. Fill in the **Item Name**, **Category**, and **Description** fields.
3. Click the **Submit** button.
4. If the submission is successful, a message will appear and the form will reset.

## Project Structure
```
project-root/
├── myproject/
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   ├── asgi.py
├── myapp/
│   ├── migrations/
│   ├── templates/
│   │    └── menu_items.html
│   ├── static/
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── tests.py
│   └── views.py
├── venv/
├── manage.py
├── README.md
├── requirements.txt
```

## Technologies Used
- **Django**: Web framework
- **MySQL**: Database
- **HTML/CSS/JavaScript**: Frontend
- **AJAX**: For smooth user experience (no page reload)

## Commands for Running & Managing the Project
| **Command**           | **Description**         |
|----------------------|------------------------|
| `python manage.py runserver` | Run the development server |
| `python manage.py makemigrations` | Create new migrations based on model changes |
| `python manage.py migrate` | Apply migrations to the database |
| `python manage.py createsuperuser` | Create an admin user for Django admin |

## Possible Issues & Troubleshooting
1. **MySQL Connection Issues**
   - Ensure your MySQL server is running.
   - Check your credentials in the `settings.py` file.

2. **Missing Dependencies**
   - Run `pip install -r requirements.txt` to ensure all dependencies are installed.

3. **Port in Use**
   - If you get a message like "Port 8000 is already in use", you can run the server on a different port using:
     ```bash
     python manage.py runserver 8080
     ```

## Contributing
1. **Fork the repository**
2. **Create a new feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Commit your changes**
   ```bash
   git add .
   git commit -m "Add your message here"
   ```
4. **Push to your branch**
   ```bash
   git push origin feature/your-feature-name
   ```
5. **Create a pull request**

## How to Push This Project to GitHub
1. **Initialize a Git repository**
   ```bash
   git init
   ```
2. **Add all files to staging**
   ```bash
   git add .
   ```
3. **Commit the changes**
   ```bash
   git commit -m "Initial commit"
   ```
4. **Add your GitHub remote**
   ```bash
   git remote add origin https://github.com/yourusername/your-repo-name.git
   ```
5. **Push the code to GitHub**
   ```bash
   git push -u origin main
   ```

## License
This project is licensed under the MIT License. See the `LICENSE` file for more information.

---

If you have any issues, feel free to open an issue on the repository. Happy coding! 🚀
