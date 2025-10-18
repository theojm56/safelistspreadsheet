# Safelist License Server (Flask)

Endpoints:
- POST /api/issue (Admin: header `X-Auth: SECRET_KEY`)
- POST /api/validate ({ key, device_id })
- POST /api/revoke (Admin: header `X-Auth: SECRET_KEY`)
- GET  /api/licenses (Admin: header `X-Auth: SECRET_KEY`)

## Local
pip install -r requirements.txt
copy .env.example to .env and set SECRET_KEY
python app.py

## Deploy (Render / Railway)
- Build: pip install -r requirements.txt
- Start: gunicorn app:app
- Env: SECRET_KEY=your-long-random-string
