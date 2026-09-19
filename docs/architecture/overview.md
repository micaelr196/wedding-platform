# Arquitectura — Visão Geral

> Estado: definida em brainstorming. Spec detalhada a escrever antes da implementação.

## As Quatro Superfícies

### 1. Landing Page
- **Tipo:** pública, não autenticada
- **Propósito:** descoberta do serviço, apresentação de features e pricing, CTA para criação de conta e subscrição de plano
- **É o topo do funil** — sem ela não há aquisição

### 2. Backoffice dos Noivos
- **Tipo:** autenticada (conta de casal)
- **Propósito:** criação e gestão do evento, editor visual do convite, dashboard de confirmações, gestão de convidados, upgrade de plano
- **Features por tier:** analytics (Platinum), galeria (Platinum), playlist (Platinum), mensagens (Platinum)

### 3. Convite Público
- **Tipo:** pública, não autenticada
- **Propósito:** o que os convidados abrem via link ou QR code; RSVP acontece aqui
- **Nota:** os convidados nunca vêem publicidade — em nenhum plano

### 4. Backend API
- **Tipo:** Go REST API
- **Propósito:** serve as três superfícies; responsável por autenticação, eventos, convites, RSVP, QR codes, pagamentos, upgrades, storage de assets

## Stack

| Componente | Tecnologia | Notas |
|---|---|---|
| Backend | Go | REST API |
| Frontend | Vue.js | Landing + Backoffice + Convite público |
| Base de dados | PostgreSQL | Relacional |
| Storage | S3-compatible | Cloudflare R2 (MVP) ou AWS S3 |
| Pagamentos | Stripe | One-time payments + upgrades diferenciais |
| Infra MVP | Docker | Railway ou Fly.io |
| Infra escala | GKE | Progressão natural dado o background da equipa |

## Editor Visual

**MVP:** Zonas editáveis com preview em tempo real — o casal personaliza campos definidos do template (texto, cores, foto de capa, data, local) e vê as alterações em directo. Parece um editor visual ao utilizador; é ordens de magnitude mais simples de construir do que um canvas livre.

**Fase 2:** Editor drag-and-drop livre (canvas tipo Canva) — após validação com os primeiros casais reais.

## Modelo de Upgrades (Pagamentos)

Upgrade = novo Stripe payment intent com o valor diferencial (ver `docs/product/pricing.md`). O plano do evento é actualizado após confirmação de pagamento via webhook Stripe.

## Decisões Fechadas

| Decisão | Escolha | Notas |
|---|---|---|
| URL do convite público | Path-based: `plataforma.pt/convite/[slug]` | Subdomínio por casal é Fase 2 / Ultra |
| Autenticação | Email + password tradicional | Magic link e OAuth (Google) são Fase 2 |

## Decisões em Aberto

- Estratégia de QR code: geração on-the-fly vs. pré-gerado e guardado
- Nome do produto (TBD)
