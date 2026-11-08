# AI Impostor — Public Deployment

Public multiplayer game for the TAMU Datathon.

## Architecture

- **Vercel**: public static frontend (`frontend/`)
- **Render**: one-worker FastAPI backend (`backend/`) for live matchmaking
- **Databricks**: AI Model Serving and Delta/SQL analytics

This repository is the public-access adaptation. The existing Databricks App is a separate deployment and is not modified here.

## Status

Repository initialized. Application source code and external hosting configuration still need to be pushed and deployed; this README does not represent a live public deployment.

## Security

Never commit `.env` files, Databricks tokens, private keys, or local virtual environments. Configure `DATABRICKS_TOKEN` in the backend hosting service's secret environment settings. The existing game state is held in memory; run a single backend worker until it is migrated to a shared database.
