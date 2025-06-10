# Sample DevOps Project

This folder contains a minimal example to demonstrate an end-to-end CI/CD pipeline using GitHub Actions.

## Folder structure

```
sample-devops-project/
├── app/
│   └── main.py
├── Dockerfile
└── .github/
    └── workflows/
        └── ci.yml
```

## Pipeline

The GitHub Actions workflow builds a Docker image for the application and runs the container whenever changes are pushed to the `main` branch or a pull request is opened.

Steps performed in `.github/workflows/ci.yml`:

1. **Checkout** the repository.
2. **Build** the Docker image with `docker build`.
3. **Run** the container to verify it starts correctly.

The Dockerfile uses Python 3.11 and copies the `app` directory. When run, the container prints a greeting.

## Running locally

To test locally, run:

```bash
docker build -t devops-demo:latest .
docker run --rm devops-demo:latest
```

This project is intentionally simple to focus on the CI/CD workflow. Extend it with tests, additional steps, or deployments as needed.
