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

**Fase:** Descoberta de produto — modelo de negócio e MVP definidos. Protótipo em construção.

## Documentação

- [`docs/product/context.md`](docs/product/context.md) — visão, mercado e princípios
- [`docs/product/pricing.md`](docs/product/pricing.md) — planos e feature matrix
- [`docs/architecture/overview.md`](docs/architecture/overview.md) — arquitectura e stack
- [`docs/research/benchmark.md`](docs/research/benchmark.md) — análise de concorrentes
- [`docs/research/interview-guide.md`](docs/research/interview-guide.md) — guia de entrevistas (PT)

- [Link LucidSpark](https://lucid.app/lucidspark/54101282-9925-4105-84ab-5299481eb333/edit?beaconFlowId=566D230D688B782F&invitationId=inv_966d2db1-c3e0-4e32-a6e6-932d8e089288&page=0_0#) - Product Discovery & Definition

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
