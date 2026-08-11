# Frontend — Dashboard Metrics

Interface React affichant les métriques en temps réel via WebSocket.

## Composants principaux

| Composant | Rôle |
|---|---|
| `Gauge` | Jauge circulaire (CPU, RAM) |
| `HistoryChart` | Graphique d'historique (Recharts) |
| `CpuCores` | Affichage par cœur |
| `ProcessTable` | Tableau des processus |
| `IOCards` | Métriques réseau et disque |
| `SystemCard` | Infos système générales |

## Hook principal

`useMetrics.ts` gère la connexion WebSocket et maintient l'état global des métriques.

## Lancer le frontend

```bash
cd metrics/frontend
npm install
npm run dev   # http://localhost:5173
```

## Build production

```bash
npm run build
```
