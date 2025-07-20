# QR Code REST API

This project implements a REST API for generating, retrieving, and deleting QR codes using FastAPI.  
It supports authentication on the OpenAPI docs, Docker containerization, and automated testing with pytest.  

---

## Project Structure

- `app/` — FastAPI application source code  
- `tests/` — Automated tests using pytest  
- `.github/workflows/production.yml` — GitHub Actions workflow for CI/CD  
- `Dockerfile` and `docker-compose.yml` — Docker container configuration  
- `start.sh` — Script to start the application  
- `requirements.txt` — Python dependencies  
- `qr.png` — Sample generated QR code image  

---

##API Endpoints
POST /qr_codes/ — Generate a new QR code

GET /qr_codes/{qr_id} — Retrieve a QR code image

DELETE /qr_codes/{qr_id} — Delete a QR code

##Running Tests
Run the test suite with:
pytest

##CI/CD with GitHub Actions
This repo includes a workflow at .github/workflows/production.yml that runs tests and builds Docker images on push.

Make sure to add your repository secrets (such as environment variables) to GitHub to allow the workflow to run correctly.

##Troubleshooting
If the app or Docker containers cannot write QR codes, verify that the qr_codes directory exists and is writable.

Ensure Docker daemon is running before using Docker Compose.

Review pytest output to diagnose test failures.
