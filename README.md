# Wedding Invitation Platform

> PaaS de convites digitais de casamento para o mercado português.

## Visão

Uma plataforma self-service que permite a qualquer casal criar, personalizar e partilhar o seu convite digital de casamento — com RSVP integrado, gestão de convidados e QR codes — sem depender de designers ou agências.

**Posicionamento:** entre o Canva (gratuito, genérico, sem RSVP) e o Digital Yes (€175–975, serviço gerido). O único produto self-service, dedicado a casamentos, com RSVP, em Portugal.

## Equipa

| Papel | Pessoa |
|---|---|
| Co-fundador / EM & Product | Micael Rosa |
| Co-fundador / Developer | Pedro Cruz |
| Feedback / Stakeholder | Catarina Gomes (noiva) |
| Feedback / Stakeholder | Ana Lobão |

## Estado

**Fase:** Descoberta de produto — brainstorming e definição do MVP concluídos. Entrevistas a 7 casais planeadas.

## Documentação

- [`docs/product/context.md`](docs/product/context.md) — visão, mercado e princípios
- [`docs/product/pricing.md`](docs/product/pricing.md) — planos e feature matrix
- [`docs/architecture/overview.md`](docs/architecture/overview.md) — arquitectura e stack
- [`docs/research/benchmark.md`](docs/research/benchmark.md) — análise de concorrentes
- [`docs/research/interview-guide.md`](docs/research/interview-guide.md) — guia de entrevistas (PT)

## Stack

| Camada | Tecnologia |
|---|---|
| Backend | Go |
| Frontend | Vue.js |
| Base de dados | PostgreSQL |
| Storage | S3-compatible (Cloudflare R2 / AWS S3) |
| Pagamentos | Stripe |
| Infra (MVP) | Docker — Railway ou Fly.io |
| Infra (escala) | GKE (Kubernetes) |

## Prior Art

[qr-welcome](https://github.com/micaelr196/qr-welcome) — solução quick-and-dirty em Go + HTML + Docker construída para a proposta de casamento do Micael. Fonte de padrões iniciais; **não é a codebase deste produto**.
