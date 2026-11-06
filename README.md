# micro-4

Prueba de integración entre Backstage y GitHub

## API

The service exposes an in-memory REST API for `items`. The OpenAPI contract is available at [`docs/openapi.yaml`](docs/openapi.yaml).

| Method | Path | Description |
| --- | --- | --- |
| `GET` | `/api/v1/items` | List all items |
| `POST` | `/api/v1/items` | Create an item |
| `GET` | `/api/v1/items/{id}` | Get an item |
| `PUT` | `/api/v1/items/{id}` | Replace an item |
| `DELETE` | `/api/v1/items/{id}` | Delete an item |

An item requires a non-empty `name` and accepts an optional `description`. Data is stored in memory and is lost when the service restarts.

## Local development

### Node.js

```bash
npm install
npm start
```

### Python

```bash
python -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
python src/app.py
```