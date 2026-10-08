# blog-fastapi

A simple blog web app built with FastAPI and Jinja2 templates.

> 🚧 Work in progress — more features coming soon.

## Features (so far)

- Home page listing blog posts
- Individual post pages
- JSON API endpoint for posts (`/posts/{post_id}`)
- Static files (CSS, JS, icons) and custom error page

## Tech Stack

- Python 3.14
- FastAPI
- Jinja2
- uv (package manager)

## Getting Started

```bash
# install dependencies
uv sync

# run the dev server
uv run fastapi dev main.py
```

Then open http://127.0.0.1:8000 in your browser.
API docs are available at http://127.0.0.1:8000/docs.

## Author

Vishesh Kathuria
