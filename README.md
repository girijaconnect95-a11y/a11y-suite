# A11Y Suite
Monorepo with:
- **backend** (FastAPI) → `http://localhost:8000/healthz`
- **frontend** (React + Vite) → `http://localhost:5173/`
- **ml-service** (FastAPI) → `http://localhost:9000/ping`

## Quick start
### Backend
cd backend
python -m venv .venv && .\.venv\Scripts\Activate.ps1
pip install fastapi "uvicorn[standard]"
python -m uvicorn src.app:app --reload --port 8000

### Frontend
cd frontend
npm install
npm run dev

### ML Service
cd ml-service
python -m venv .venv && .\.venv\Scripts\Activate.ps1
pip install fastapi "uvicorn[standard]"
python -m uvicorn src.service:app --reload --port 9000
