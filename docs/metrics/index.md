# Metrics — Présentation

Dashboard de métriques système en temps réel.

## Stack

- **Backend** : FastAPI + `psutil`
- **Frontend** : React + TypeScript + Vite
- **Visualisation** : Recharts

## Lancer le projet

=== "Backend"

    ```bash
    cd metrics/backend
    pip install -r requirements.txt
    uvicorn main:app --reload
    ```

=== "Frontend"

    ```bash
    cd metrics/frontend
    npm install
    npm run dev
    ```
