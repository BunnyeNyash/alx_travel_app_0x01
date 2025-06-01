# ALX Travel App: Milestone 1 - Setup and Database Configuration

## Overview

This project is Milestone 1 of the ALX ProDev Backend Python curriculum, establishing the foundation for the `alxtravelapp`, a Django-based travel listing platform. The milestone focuses on initializing a Django project named `alx_travel_app`, creating a `listings` app, configuring a MySQL database with environment variables, integrating Swagger for API documentation, and setting up version control with Git. The setup employs industry-standard practices for scalable backend development, secure configuration management, and automated API documentation.

## Objectives

- Initialize a Django project (`alx_travel_app`) with a modular, production-ready structure.
- Create a `listings` app to encapsulate core functionalities.
- Configure MySQL as the primary database using `django-environ` for secure environment variable management.
- Integrate Swagger (via `drf-yasg`) for automated API documentation accessible at `/swagger/`.
- Set up REST framework and CORS headers for API support.
- Establish a Git repository for version control and collaboration.

## Repository

- **GitHub Repository**: [alx_travel_app](https://github.com/BunnyeNyash/alx_travel_app.git)
- **Directory**: `alx_travel_app`

## Directory Structure

```
alx_travel_app/
├── alx_travel_app/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py        # Django settings with MySQL and Swagger configuration
│   ├── urls.py           # URL routing with Swagger endpoints
│   ├── wsgi.py
├── listings/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── migrations/
│   │   ├── __init__.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py           # App-specific URL configuration
│   ├── views.py
├── .env                  # Environment variables for secure configuration
├── .gitignore            # Git ignore file for Python/Django projects
├── requirements.txt      # Project dependencies
├── manage.py             # Django management script
```

## Prerequisites

- **Python**: Version 3.8 or higher
- **MySQL**: MySQL Server 8.0 or compatible
- **Git**: For version control
- **Python Libraries** (listed in `requirements.txt`):
  - `django`: Core framework
  - `djangorestframework`: REST API development
  - `django-cors-headers`: CORS support
  - `drf-yasg`: Swagger API documentation
  - `celery`: For future task queuing
  - `mysqlclient`: MySQL database adapter
  - `django-environ`: Environment variable management

## File Descriptions

- **requirements.txt**: Lists project dependencies, including `django`, `djangorestframework`, `django-cors-headers`, `drf-yasg`, `celery`, `mysqlclient`, and `django-environ`.
- **alx_travel_app/settings.py**: Configures Django settings, including MySQL database, REST framework, CORS headers, and Swagger integration using `django-environ` for environment variables.
- **alx_travel_app/urls.py**: Defines URL patterns, including admin, API routes, and Swagger/ReDoc endpoints.
- **listings/urls.py**: Placeholder for app-specific API endpoints.
- **.env**: Stores environment variables (e.g., database credentials, secret key) for secure configuration.
- **.gitignore**: Excludes Python, Django, and environment files from version control.
- **manage.py**: Django’s command-line utility for managing the project.

