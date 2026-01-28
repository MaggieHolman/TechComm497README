# 🌱 Rooted

Helping immigrants connect with local communities through shared interests and events.

Rooted is a Python + Flask web application designed to help immigrants discover local events and community opportunities based on their interests and location. The goal is to reduce social isolation by making it easier to meet people and feel connected in a new place.

**Who this is for**
- Immigrants and newcomers looking to build community
- People starting jobs in a new area
- International Students

## Table of Contents
- [Quickstart](#quickstart)
- [Features](#features)
- [Architecture](#architecture)
- [Usage](#usage)
- [FAQ](#faq)
- [Future Work](#future-work)

## Quick start

1. Create a virtual environment and install dependencies:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

2. (Optional) create a `.env` file or export env vars. Example `.env`:

```
DATABASE_URL=sqlite:///./data.db
SECRET_KEY=replace-with-a-secret
UPLOAD_FOLDER=./static/uploads
```

3. Run the app:

```bash
python app.py
```

4. Visit `http://127.0.0.1:5000` — you'll be redirected to the login page. Use the signup page to create an account.

## Features
- User signup and login with secure password hashing
- Session-based authentication
- Profile image uploads
- Event discovery based on user interests (planned/partial)

## Architecture

Rooted is built as a server-rendered Flask application with session-based authentication and a relational database backend.

![Architecture diagram](path/to/architecture-diagram.png)

At a high level:
- Users interact through a browser using HTML forms
- Flask routes handle requests and authentication
- SQLAlchemy manages persistence for users and events
- Uploaded images are stored on the server filesystem

## Usage

1. Create an account using the signup form
2. Log in with your credentials
3. Upload a profile image
4. Browse events related to your interests


## FAQ

**Why Flask instead of Django?**  
Flask allowed us to build and iterate quickly with minimal overhead.

**Can this use Postgres instead of SQLite?**  
Yes. Set `DATABASE_URL` to a Postgres connection string.

**How is authentication handled?**  
Using Flask sessions with securely hashed passwords.

## Future Work
- Recommendation system for events
- OAuth login
- Improved accessibility and localization
