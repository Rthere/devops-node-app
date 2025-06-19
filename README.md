# DevOps Node.js App 🚀

This project demonstrates a complete DevOps pipeline using **Node.js**, **Docker**, and **GitHub Actions**. It includes a simple Express.js web application that is containerized with Docker and automatically built and deployed through a CI/CD pipeline on every push to the `main` branch.

---

## 🔧 Tech Stack

- **Node.js** (Express)
- **Docker** (Containerization)
- **GitHub Actions** (Primary CI/CD tool)
- **Docker Hub** (Image Registry)
- *Optional: CircleCI (Alternative CI/CD tool if required)*

---

## 📁 Project Structure

```
devops-node-app/
├── app.js                   # Express web server
├── Dockerfile               # Docker configuration
├── package.json             # Node.js dependencies
├── .github/workflows/       # GitHub Actions pipeline
│   └── deploy.yml
└── k8s/                     # (Optional) Kubernetes manifests
    ├── deployment.yaml
    └── service.yaml
```

---

## 🚀 Run Locally

### Install dependencies
```bash
npm install
```

### Start the app
```bash
node app.js
```

Visit: [http://localhost:3000](http://localhost:3000)

---

## 🐳 Run in Docker

### Build Docker image
```bash
docker build -t rthere/devops-node-app:latest .
```

### Run Docker container
```bash
docker run -p 3000:3000 rthere/devops-node-app
```

---

## ⚙️ CI/CD with GitHub Actions

The pipeline automatically builds the Docker image and pushes it to Docker Hub when code is pushed to the `main` branch.

### Secrets used in GitHub:
- `DOCKER_USERNAME`
- `DOCKER_PASSWORD`

Stored securely in:
`Settings → Secrets → Actions`

---

## 📦 Docker Image

View the public image here:  
👉 [Docker Hub - rthere/devops-node-app](https://hub.docker.com/repository/docker/rthere/devops-node-app)

---

## 🔁 Optional: CircleCI Support

If preferred, the pipeline can also be run on **CircleCI** with a config like:
```yaml
.circleci/config.yml
```

Use CircleCI dashboard to connect your GitHub repo and configure secrets for:
- `DOCKER_USER`
- `DOCKER_PASS`

---

## ✅ Future Improvements

- Add unit tests to CI/CD
- Deploy to Minikube or EKS
- Monitor with Prometheus + Grafana
- Add staging and production environments

---

## 🙌 Author

**Rohan Tathe**  
[GitHub](https://github.com/Rthere) ・ [LinkedIn](https://www.linkedin.com/in/rohan-tathe-2593b526a/)
