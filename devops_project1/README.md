# DevOps Project 1

This directory contains a basic DevOps project to demonstrate an end-to-end CI/CD pipeline using GitHub Actions.

## Structure

```
devops_project1/
├── app/
│   └── main.py
├── Dockerfile
└── .github/
    └── workflows/
        └── ci.yml
```

## Pipeline

The GitHub Actions workflow builds a Docker image and runs the container when changes are pushed to the `main` branch or a pull request is opened.

Steps in `.github/workflows/ci.yml`:

1. **Checkout** the repository.
2. **Build** the Docker image using `docker build`.
3. **Run** the container to verify it starts correctly.

Extend this project with your own tests and deployment steps as you learn more about DevOps practices.
