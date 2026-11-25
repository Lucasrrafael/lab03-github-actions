# Laboratório 03 — GitHub Actions: testes e containers (CI/CD · Web Academy UFAM)

## Exercício 01 — Testes com Jest e cobertura de código

Pasta [`lab03_01`](lab03_01): projeto TypeScript testado com Jest (`ts-jest`), com relatório de cobertura.

Workflow [`teste.yml`](.github/workflows/teste.yml) (**Test Pipe**), disparado por push na `main`:
roda os testes com cobertura em uma *matrix* com Node.js 16.x e 18.x.
