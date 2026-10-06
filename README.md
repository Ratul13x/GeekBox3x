# GeekBox3

GeekBox3 is a Flask-based web application packaged in this repository as a ZIP archive (`GeekBox3-main.zip`). The project appears to be a small database-driven web app with user-facing forms, SQLite storage, and static media uploads.

## Overview

This application includes:

- A Flask app entrypoint in `app.py`
- SQLite-backed data storage under `instance/geekbox.db`
- Model and form definitions in `models.py` and `forms.py`
- Static styling and uploaded image assets in `static/`
- Gunicorn deployment config via `Procfile`
- Python dependency management via `requirements.txt`

## Project structure

```text
GeekBox3-main/
├── app.py
├── config.py
├── forms.py
├── models.py
├── pics.txt
├── requirements.txt
├── Procfile
├── instance/
│   └── geekbox.db
├── static/
│   ├── style.css
│   └── uploads/
│       ├── 1.PNG
│       └── 2.PNG
└── README.md
```

## Requirements

- Python 3.9+
- pip

Install dependencies:

```bash
pip install -r requirements.txt
```

## Run locally

1. Extract the repository ZIP if needed:

```bash
unzip GeekBox3-main.zip
cd GeekBox3-main
```

2. Start the Flask app:

```bash
python app.py
```

3. Open the app in a browser at:

```text
http://127.0.0.1:5000
```

## Production/deployment

A `Procfile` is included for deployment with Gunicorn. The project is configured to run as a WSGI app using the Flask application object.

Example:

```bash
gunicorn app:app
```

## Notes

- The app uses SQLite for local persistence.
- Media uploaded by users is stored in the `static/uploads/` directory.
- This repository currently contains the packaged source archive; extracting it before development is recommended.

## License

No explicit license file is present in the packaged project. If you are using or distributing this code, check the original project source for any licensing requirements.
