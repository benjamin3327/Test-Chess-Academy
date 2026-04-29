 # Copilot Instructions
 
 ## Project Overview
 Chess Academy — a website for learning and registering for chess courses. Frontend built with Vite + React + Tailwind 
CSS; backend with Python/FastAPI.
 
 ## Repository Structure
 ```
 /
 ├── frontend/        # Vite + React app
 ├── backend/         # FastAPI app
 └── .github/
     └── copilot-instructions.md
 ```
 
 ## Frontend (Vite + React + Tailwind CSS)
 
 ### Dev server
 ```bash
 cd frontend
 npm install
 npm run dev
 ```
 
 ### Build
 ```bash
 npm run build
 ```
 
 ### Conventions
 - Components live in `frontend/src/components/`, pages in `frontend/src/pages/`
 - Use functional components with hooks — no class components
 - Style exclusively with Tailwind utility classes; avoid inline styles and separate CSS files
 - Keep component files co-located with their tests (`ComponentName.test.tsx` alongside `ComponentName.tsx`)
 
 ## Backend (Python + FastAPI)
 
 ### Dev server
 ```bash
 cd backend
 pip install -r requirements.txt
 uvicorn main:app --reload
 ```
 
 ### Run a single test
 ```bash
 pytest tests/test_<module>.py::test_<function_name> -v
 ```
 
 ### Run all tests
 ```bash
 pytest
 ```
 
 ### Conventions
 - Route handlers live in `backend/routers/`, shared models in `backend/models/`
 - Use Pydantic models for all request/response schemas
 - Auth uses JWT tokens — pass as `Authorization: Bearer <token>` header
 
 ## Key Features to Build
 - User registration and login
 - Course catalog and lesson pages
 - Student progress tracking
