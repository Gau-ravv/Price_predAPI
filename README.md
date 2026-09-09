# 🚗 Car Price Prediction API

A production-ready, **Machine Learning REST API** built with **FastAPI** to estimate used car market values in real time. Designed for scalability and maintainability, this service features JWT/API-key authentication, Redis response caching, and full observability integration.

---

## 🛠️ Tech Stack & Architecture

* **Framework:** [FastAPI](https://fastapi.tiangolo.com/) (Python)
* **Caching:** [Redis](https://redis.io/)
* **Monitoring & Metrics:** [Prometheus](https://prometheus.io/) + [Grafana](https://grafana.com/)
* **Containerization:** [Docker](https://www.docker.com/) & Docker Compose
* **Cloud Platform:** [Render](https://render.com/)

---

## ✨ Key Features

- 🔐 **Dual Security Layer:** Supports both JWT token authentication and dedicated API key headers.
- ⚡ **High-Performance Caching:** Integrated Redis layer to eliminate redundant inference calculations for duplicate requests.
- 📊 **Built-in Observability:** Exposes Prometheus metrics out of the box with ready-to-use Grafana dashboards.
- 🐳 **Containerized Deployment:** Fully orchestrated via Docker Compose for uniform development and production setups.

---

## 🧠 Model Input Schema

The predictive engine accepts the following JSON schema features:

| Feature | Data Type | Description | Example |
| :--- | :--- | :--- | :--- |
| `company` | `string` | Vehicle manufacturer/brand | `"Maruti"` |
| `year` | `integer` | Year of manufacture | `2015` |
| `owner` | `string` | Previous ownership status | `"Second"` |
| `fuel` | `string` | Fuel type (`Petrol`, `Diesel`, `CNG`, etc.) | `"Petrol"` |
| `seller_type` | `string` | Seller category (`Individual` or `Dealer`) | `"Individual"` |
| `transmission` | `string` | Transmission category (`Manual` or `Automatic`) | `"Automatic"` |
| `km_driven` | `integer` | Total distance driven (in km) | `200000` |
| `mileage_mpg` | `float` | Fuel efficiency (in MPG) | `55.0` |
| `engine_cc` | `float` | Engine displacement (in CC) | `1250.0` |
| `max_power_bhp` | `float` | Peak power output (in BHP) | `80.0` |
| `torque_nm` | `float` | Peak engine torque (in Nm) | `200.0` |
| `seats` | `integer` | Seating capacity | `5` |

---

## 🚀 Getting Started (Local)

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/fastapi-project.git
cd fastapi-project
```

### 2. Set Environment Variables

```bash
API_KEY=demo-key
JWT_SECRET_KEY=your-secret
REDIS_URL=redis://localhost:6379
```

### 3. Build and Run via Docker

```bash
docker-compose up --build
```

### 4. Access Interfaces

- FastAPI Docs: http://localhost:8000/docs
- FastAPI Metrics: http://localhost:8000/metrics
- Prometheus UI: http://localhost:9090
- Grafana UI: http://localhost:3000

