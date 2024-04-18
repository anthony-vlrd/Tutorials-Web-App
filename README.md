# Django Web Application

This project is a Django-based web application designed to be deployed on Google Cloud. It includes configurations for Docker and Google Cloud deployment settings, making it suitable for production environments.
GCP services used in this workshop include: Cloud Run, Cloud Build, Cloud SQL, Artifact Registry, Secret Manager, and more.

## Prerequisites

- Python 3.8 or higher
- Docker
- A Google Cloud account with the necessary permissions for App Engine deployment

## Installation

1. **Clone the Repository:**

2. **Install Dependencies:**
- Ensure you have Python and Docker installed on your system.
- Install Python dependencies by running:
  ```
  pip install -r requirements.txt
  ```

## Configuration

- Configure the Django settings:
- Adjust the settings in `settings.py` to fit your production or development needs.
- Configure database settings and other environmental variables in `settings.py` using `django-environ`.

- Prepare your Docker environment:
- Use the provided `Dockerfile` to build the Docker image.

## Running the Application

1. **Local Deployment:**
- To run the Django application locally:
  ```
  python manage.py runserver
  ```

2. **Docker:**
- Build the Docker image:
  ```
  docker build -t mydjangoapp .
  ```
- Run the Docker container:
  ```
  docker run -p 8000:8000 mydjangoapp
  ```

## Deploying to Google Cloud

- Configure your Google Cloud settings in the `cloudmigrate.yml` file.
- Use the Google Cloud CLI to deploy the application:


## Additional Information

- This application uses Django 3.2.2, DRF 3.12.4 for API management, and `psycopg2-binary` for PostgreSQL database connections.
- It is configured to work with Google Cloud Secret Manager and Django Storages for file management.












