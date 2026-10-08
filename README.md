# blog-fastapi

A full-stack blog application built with **FastAPI**, featuring a server-rendered frontend, a REST API, JWT authentication, PostgreSQL, cloud file storage, automated tests and production deployment.

## Features

- **Web app + REST API** – Jinja2-rendered pages alongside a JSON API
- **Validation & error handling** – typed path/query parameters, custom error pages
- **Pydantic schemas** – request and response validation
- **Database** – SQLAlchemy models and relationships, full CRUD (GET, POST, PUT, PATCH, DELETE)
- **Async** – asynchronous routes and database access
- **Modular routing** – routes organized with `APIRouter`
- **Frontend forms** – JavaScript connected to the API
- **Authentication** – user registration and login with JWT
- **Authorization** – protected routes and current-user verification
- **File uploads** – profile image processing, validation and storage
- **Pagination** – loading more posts with query parameters
- **Password reset** – email tokens and background tasks
- **Migrations** – PostgreSQL with Alembic
- **Cloud storage** – uploads stored on AWS S3 via Boto3
- **Testing** – Pytest, fixtures and mocking of external services
- **Deployment** – VPS (Nginx, SSL, custom domain) and Docker containers

## Tech Stack

| Area        | Tools                                  |
|-------------|----------------------------------------|
| Backend     | Python 3.14, FastAPI, Pydantic         |
| Frontend    | Jinja2, HTML, CSS, JavaScript          |
| Database    | PostgreSQL, SQLAlchemy, Alembic        |
| Auth        | JWT, password hashing                  |
| Storage     | AWS S3, Boto3                          |
| Testing     | Pytest                                 |
| DevOps      | Docker, Nginx, uv                      |

## Project Structure

```
fastapi_blog/
├── main.py            # App entry point
├── routers/           # API and page routes
├── models.py          # SQLAlchemy models
├── schemas.py         # Pydantic schemas
├── alembic/           # Database migrations
├── templates/         # Jinja2 templates
├── static/            # CSS, JS, icons, images
├── tests/             # Pytest test suite
└── pyproject.toml
```

## Getting Started

### Prerequisites

- Python 3.14+
- [uv](https://docs.astral.sh/uv/)
- PostgreSQL

### Installation

```bash
git clone https://github.com/ViShEsHK2412/blog-fastapi.git
cd blog-fastapi
uv sync
```

### Configuration

Create a `.env` file in the project root:

```env
DATABASE_URL=postgresql://user:password@localhost:5432/blog
SECRET_KEY=your-secret-key
AWS_ACCESS_KEY_ID=your-access-key
AWS_SECRET_ACCESS_KEY=your-secret-key
S3_BUCKET_NAME=your-bucket
MAIL_USERNAME=your-email
MAIL_PASSWORD=your-email-password
```

### Run

```bash
uv run alembic upgrade head     # apply migrations
uv run fastapi dev main.py      # start the dev server
```

- App: http://127.0.0.1:8000
- API docs: http://127.0.0.1:8000/docs

### Tests

```bash
uv run pytest
```

### Docker

```bash
docker build -t blog-fastapi .
docker run -p 8000:8000 --env-file .env blog-fastapi
```

## Acknowledgements

Built while following Corey Schafer's [FastAPI Tutorials](https://www.youtube.com/@coreyms) series.

## Author

**Vishesh Kathuria** – [GitHub](https://github.com/ViShEsHK2412)
