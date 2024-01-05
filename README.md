# Django Development Templates

## Installation

1. Create a virtual environment:

    ```bash
    virtualenv venv
    ```

2. Clone the project:

    ```bash
    git clone https://github.com/F4ruk-seker/django-development-templates/tree/standard_django_template
    ```

3. Install the requirements:

    ```bash
    cd project_folder
    source venv/bin/activate  # or venv\Scripts\activate (Windows)
    pip install -r requirements.txt
    ```

4. Create a `.env` file:

    Create a file named `.env` in the project root and configure the necessary environment variables. You can refer to the `.env.example` file for a template.

    Example of generating a random `SECRET_KEY`:

    ```bash
    python -c "import random; print('DJANGO_SECRET_KEY=' + ''.join(random.SystemRandom().choice('abcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*(-_=+)') for i in range(50)))" >> .env
    ```

    This will generate a random `DJANGO_SECRET_KEY` and append it to the `.env` file.

5. Run the Django project:

    ```bash
    python manage.py runserver
    ```

6. View the project in your browser:

    [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

7. Apply database migrations:

    ```bash
    python manage.py makemigrations
    python manage.py migrate
    ```

8. Create a superuser account:

    ```bash
    python manage.py createsuperuser
    ```

    You can log in to the [Admin Panel](http://127.0.0.1:8000/admin/) with the credentials you provided.
