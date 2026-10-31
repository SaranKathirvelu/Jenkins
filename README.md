# Northstar landing page

A responsive landing page built with Flask and packaged to run in Docker.

## Run with Docker

```powershell
docker build -t northstar-web .
docker run --rm -p 8000:8000 northstar-web
```

Open [http://localhost:8000](http://localhost:8000). The container health endpoint is available at `/healthz`.

## Run locally

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python app.py
```

The Flask development server listens on `http://localhost:8000`. Docker runs the app with Gunicorn.
