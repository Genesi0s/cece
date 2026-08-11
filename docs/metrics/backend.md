# Backend — API Metrics

API REST + WebSocket exposant les métriques système en temps réel.

## Endpoints

### `GET /metrics`

Retourne un snapshot instantané de toutes les métriques.

```json
{
  "cpu_per_core": [12.5, 8.0, 45.2, 3.1],
  "cpu_freq_mhz": 2400,
  "memory_percent": 67.3,
  "disk_percent": 42.0,
  "net_bytes_sent": 1024000,
  "net_bytes_recv": 2048000
}
```

### `WebSocket /ws`

Flux temps réel, push toutes les secondes.

```js
const ws = new WebSocket("ws://localhost:8000/ws");
ws.onmessage = (event) => console.log(JSON.parse(event.data));
```

## Stack technique

| Dépendance | Rôle |
|---|---|
| `fastapi` | Framework web |
| `psutil` | Lecture des métriques système |
| `uvicorn` | Serveur ASGI |

## Lancer le serveur

```bash
cd metrics/backend
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
```

!!! note "CORS"
    Le serveur autorise par défaut les origines `localhost:5173` et `localhost:3000`.
