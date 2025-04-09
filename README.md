# hsa13-hw23-ci-cd
Setup CI/CD for your pet project or project based on laradock.

# CI/CD Demo Project

[![CI/CD Pipeline](https://github.com/kovamaru/hsa13-hw23-ci-cd/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/kovamaru/hsa13-hw23-ci-cd/actions/workflows/ci-cd.yml)

- `/hello` endpoint returns "Hello!"
- Unit + Integration test with MockMvc
- Dockerfile for building image
- GitHub Actions pipeline:
    - Runs tests on push
    - Builds and pushes Docker image to GitHub Container Registry on `main`

## Deployment Strategy

**Recreate Deployment:**  
The container is stopped and recreated from scratch on each deployment.  
This is implemented via Docker image rebuild and push (actual deployment not included in this repo).

## Example API

```bash
curl http://localhost:8080/hello
# Output: Hello!
