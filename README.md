# TaskFlow

Aplikasi manajemen task sederhana dengan FastAPI (backend) dan PHP (frontend).

## Struktur Proyek

```
taskflow/
├── backend/          # FastAPI + SQLite
├── frontend/         # PHP + Vanilla JS
└── tests/
    ├── postman/      # API collection
    ├── selenium/     # UI testing
    └── performance/  # Load testing dengan Locust
```

## Cara Menjalankan

### Backend
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
# API berjalan di http://localhost:8000
```

### Frontend
```bash
cd frontend
php -S localhost:8080
# Buka http://localhost:8080
```

### Testing

**Unit test (pytest):**
```bash
cd backend
pytest test_api.py -v
```

**Postman:**
Import `tests/postman/TaskFlow_API_Collection.json` ke Postman.

**Selenium:**
```bash
cd tests/selenium
pytest test_frontend.py -v
```

**Load test (Locust):**
```bash
cd tests/performance
locust -f locustfile.py
# Buka http://localhost:8089
```
