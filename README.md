# Estudo DevOps

Repositório criado para consolidar estudos e práticas de DevOps com foco em performance, segurança, observabilidade e automação. No momento, o conteúdo está focado em Docker, mas o objetivo é evoluir com materiais e exemplos de Kubernetes, Prometheus, Grafana, GitHub Actions e outros componentes do ecossistema.

## Objetivos
- Explorar e documentar práticas de DevOps aplicadas a projetos reais
- Manter exemplos práticos e reprodutíveis (infra como código sempre que possível)
- Comparar alternativas e registrar trade-offs
- Focar em escalabilidade, confiabilidade e custo-benefício na nuvem

## Status atual
- Conteúdo inicial: Docker (multistage build)
- Caminho do exemplo atual: `docker/Dockerfile.multistage`

## Conteúdos planejados
- Docker: boas práticas de build, segurança de imagens, multi-stage
- Kubernetes: deployments, services, ingress, configmaps/secrets, health checks
- Observabilidade: Prometheus (métricas), Grafana (dashboards), Alertmanager (alertas)
- CI/CD: GitHub Actions (pipelines, cache, estratégias de deploy)
- Infraestrutura: Terraform (IaC) e provisionamento básico
- Extras: Helm, Kustomize, testes de carga, scanners de segurança (Trivy, Snyk)

## Estrutura do projeto
```
estudo_devops/
  └─ docker/
      └─ Dockerfile.multistage
```

## Pré-requisitos
- Docker 24+ e Docker Buildx habilitado
- Git

## Como começar
1) Clone o repositório:
```bash
git clone https://github.com/<seu-usuario>/estudo_devops.git
cd estudo_devops
```

2) Faça o build da imagem de exemplo (multistage):
```bash
docker build -f docker/Dockerfile.multistage -t estudo-devops:latest .
```

3) Rode um contêiner (ajuste porta/comando conforme sua app):
```bash
docker run --rm -it -p 8080:8080 estudo-devops:latest
```

## Roadmap
- [ ] Docker: camadas otimizadas, SBOM, scanning de vulnerabilidades
- [ ] Kubernetes: manifests básicos + Helm charts
- [ ] Observabilidade: stack Prometheus + Grafana com dashboards base
- [ ] CI/CD: pipeline no GitHub Actions (build, test, scan, push)
- [ ] Infra: Terraform para provisionamento mínimo
- [ ] Documentação: guias de troubleshooting e boas práticas

## Contribuição
- Sugestões e PRs são bem-vindos.
- Mantenha exemplos mínimos, reproduzíveis e com instruções claras.

## Boas práticas pretendidas
- Imagens mínimas, imutáveis e assinadas quando possível
- Configuração via variáveis de ambiente e secrets
- Health checks, readiness/liveness em K8s
- Observabilidade desde o início (métricas, logs, tracing)
- Pipelines com gates de qualidade e segurança

## Referências úteis
- Docker: [https://docs.docker.com](https://docs.docker.com)
- Kubernetes: [https://kubernetes.io/docs](https://kubernetes.io/docs)
- Prometheus: [https://prometheus.io/docs](https://prometheus.io/docs)
- Grafana: [https://grafana.com/docs](https://grafana.com/docs)
- GitHub Actions: [https://docs.github.com/actions](https://docs.github.com/actions)

---
Sinta-se à vontade para abrir issues com dúvidas e ideias de novos tópicos. 