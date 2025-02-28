# Microservices Architecture with Submodules

This repository serves as the **main entry point** for managing multiple microservices using **Git submodules**. It includes:

- **API Gateway** (`api-gateway`)
- **Authentication Service** (`auth-service`)
- **Product Service** (`product-service`)

Each service is stored as a **separate repository** and linked here via Git submodules.

## 🚀 Getting Started

### 🔹 Clone the Repository (with Submodules)
To clone this repository along with all submodules, run:

```sh
git clone --recurse-submodules https://github.com/your-org/microservices-repo.git
cd microservices-repo
```

If you already cloned the repo but forgot to include submodules, run:

```sh
git submodule update --init --recursive
```

## 🛠 Managing Submodules

### 🔄 Pulling Latest Updates from Submodules
When working on the project, always fetch the latest updates:

```sh
git submodule update --remote --merge
```

Alternatively, you can pull updates for all submodules and commit them:

```sh
git submodule foreach git pull origin main
git commit -am "Updated submodules"
git push origin main
```

### 🆕 Adding a New Submodule
If you need to add another microservice, use:

```sh
git submodule add https://github.com/your-org/new-microservice.git new-microservice
git commit -m "Added new microservice"
git push origin main
```

## 🐳 Running with Docker Compose
You can run all microservices together using Docker:

```sh
docker-compose up --build -d
```

To stop all running services:

```sh
docker-compose down
```

## 🔧 Troubleshooting

1️⃣ **Submodule folder is empty?**  
Run:
```sh
git submodule update --init --recursive
```

2️⃣ **Need to reset submodules?**  
Run:
```sh
git submodule deinit -f .
git submodule update --init --recursive
```

## 📜 License
This project is licensed under the MIT License.
