# Laboratório 03 — GitHub Actions: testes e containers (CI/CD · Web Academy UFAM)

## Exercício 01 — Testes com Jest e cobertura de código

Pasta [`lab03_01`](lab03_01): projeto TypeScript testado com Jest (`ts-jest`), com relatório de cobertura.

Workflow [`teste.yml`](.github/workflows/teste.yml) (**Test Pipe**), disparado por push na `main`:
roda os testes com cobertura em uma *matrix* com Node.js 16.x e 18.x.

## Exercício 02 — Containers com GitHub Actions

Pasta [`lab03_docker`](lab03_docker): aplicação Express ("Bem vindos ao WebAcademy!!") com `Dockerfile`.

Workflow [`docker_build.yml`](.github/workflows/docker_build.yml) (**Build on DockerHub**), disparado por push na `main`:
faz o build da imagem com Docker Buildx, autentica no Docker Hub com as secrets
`DOCKERHUB_USERNAME`/`DOCKERHUB_TOKEN` e publica a imagem
[`lucasrrafael/webacademy:latest`](https://hub.docker.com/r/lucasrrafael/webacademy).

Para rodar a imagem publicada: `docker compose -f lab03_docker/docker-compose.yml up -d` (porta 80).
