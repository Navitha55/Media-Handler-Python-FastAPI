# Media Handler | FastAPI + Streamlit + ImageKit

A media-sharing application built with **FastAPI, Streamlit, SQLite, and ImageKit**. Users can upload images and videos with captions, store media files in ImageKit, and retrieve uploaded posts through a feed.

## 🚀 Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| FastAPI | Backend REST API |
| Streamlit | Frontend user interface |
| SQLite | Database for storing post information |
| SQLAlchemy | Database ORM and query management |
| ImageKit | Cloud storage and media delivery |
| Uvicorn | ASGI server |
| uv | Python dependency and project management |

## ✨ Features

- Upload images and videos.
- Add captions to uploaded media.
- Store media files in ImageKit.
- Save media URLs and post information in SQLite.
- Retrieve uploaded posts through a feed API.
- Interact with the backend through a Streamlit frontend.

## 📁 Project Structure

```text
Media-Handler-Python-FastAPI/
│
├── main.py
├── frontend.py
├── pyproject.toml
├── uv.lock
├── .env.example
├── .gitignore
│
└── src/
    ├── __init__.py
    ├── app.py
    ├── images.py
    ├── models.py
    ├── schema.py
    ├── users.py
    └── media_handler_python_fastapi/
        └── __init__.py
```

*Note: Update the structure if your actual frontend filename or project files differ.*

## ⚙️ Prerequisites

- Python 3.13 or compatible version
- uv
- ImageKit account and API credentials

## 🗄️ Database

SQLite is used to store post metadata, including:

- Post ID
- Caption
- Image or video URL
- File type
- File name
- Creation timestamp

The actual media files are stored in ImageKit. SQLite stores their associated information and URLs.

## ☁️ ImageKit Integration

ImageKit handles media storage and delivery.

The backend:
1. Receives an uploaded file from the client.
2. Processes the file for upload.
3. Sends the file to ImageKit.
4. Receives the media URL and file details.
5. Saves the corresponding post information in SQLite.

## 🧩 Application Architecture

```text
                 User
                   |
                   v
            Streamlit Frontend
                   |
              HTTP Requests
                   |
                   v
             FastAPI Backend
                   |
           +-------+-------+
           |               |
           v               v
        ImageKit         SQLite
      Media Storage    Post Metadata
```

## 📌 Future Improvements

- User authentication and authorization.
- Delete uploaded posts.
- Media preview and improved feed UI.
- File size and format validation.
- Pagination for feed results.
- Better error handling and logging.
- Docker-based deployment.
