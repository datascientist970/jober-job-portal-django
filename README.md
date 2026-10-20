# Jober — Job Portal (Django)

A Django job portal with two user roles — **Job Seekers** and **Employers** — built around a custom user model. Employers post jobs with images, job seekers browse listings and apply with a cover letter.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?logo=sqlite&logoColor=white)

## Overview

Jober was originally developed inside a Django projects collection and now lives in its own repository. It demonstrates role-based authentication, relational modelling between employers, jobs and applications, file uploads (resumes and job images), and a themed admin panel (Grappelli).

## Key Features

- **Custom user model** (`CustomUser`) with `jobseeker` / `employer` user types
- **Employer profiles** with company name; employers create and manage job postings
- **Job listings** with title, description, location, salary, category and image
- **Applications** — seekers apply with name, email and cover letter (`JobApplication`)
- **Resume upload** on the job-seeker profile
- **Grappelli-themed admin** with a custom index dashboard
- Bootstrap-based templates: home, register, login, apply, share job

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python, Django |
| Admin theme | django-grappelli |
| Database | SQLite (development) |
| Frontend | HTML, Bootstrap templates |
| Media | Django file/image uploads (Pillow) |

## Project Structure

```
├── jober/          # Project settings, URLs, WSGI/ASGI
├── jobs/           # App: models, views, URLs, migrations
│   └── models.py   # CustomUser, Employer, JobSeeker, Job, JobApplication
├── templates/      # home, register, login, apply, share_job, admin
├── dashboard.py    # Grappelli custom dashboard
└── manage.py
```

## Getting Started

```bash
git clone https://github.com/datascientist970/jober-job-portal-django.git
cd jober-job-portal-django
python -m venv venv && source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Open http://127.0.0.1:8000/ and register as a job seeker or employer.

## Notes

- The development database (`db.sqlite3`) and uploaded media are intentionally not tracked — run `migrate` to create a fresh database.
- This project was split out of the `Web-Development-Django-` collection for easier discovery and development.

## Author

**Muhammad Dawood** — AI & Data Science Engineer | Full-Stack Developer
GitHub: https://github.com/datascientist970 · LinkedIn: https://www.linkedin.com/in/dawood406/
Mardan, Khyber Pakhtunkhwa, Pakistan
