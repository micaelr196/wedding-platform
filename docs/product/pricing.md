# Modelo de Pricing

## Estrutura de Planos

Todos os planos são **pagos por evento**, **pré-pagos no acto de criação do evento**.

| Feature | Light €75 | Premium €150 | Platinum €230 |
|---|:---:|:---:|:---:|
| **Retenção do evento** | Até D+1 (dia após casamento) | 1 ano pós-evento | 1 ano pós-evento |
| Editor visual (zonas editáveis + preview) | ✅ | ✅ | ✅ |
| Templates (3–5) | ✅ | ✅ | ✅ |
| RSVP + restrições alimentares | ✅ | ✅ | ✅ |
| Dashboard de confirmações | ✅ | ✅ | ✅ |
| QR code único (partilha geral) | ✅ | ✅ | ✅ |
| Programa do dia | ✅ | ✅ | ✅ |
| Google Ads no backoffice | ✅ | ❌ | ❌ |
| Sem publicidade | ❌ | ✅ | ✅ |
| QR codes por convidado (personalizados) | ❌ | ✅ | ✅ |
| Export CSV de convidados | ❌ | ✅ | ✅ |
| Playlist personalizada | ❌ | ❌ | ✅ |
| Mensagens entre convidados | ❌ | ❌ | ✅ |
| Galeria colaborativa (upload por convidados) | ❌ | ❌ | ✅ |
| Analytics avançado | ❌ | ❌ | ✅ |
| Página de alojamento | ❌ | ❌ | ✅ |

## Upgrades

O upgrade é sempre possível dentro do mesmo evento. O valor cobrado é **a diferença entre planos**:

| De → Para | Valor cobrado |
|---|---|
| Light → Premium | €75 (€150 − €75) |
| Light → Platinum | €155 (€230 − €75) |
| Premium → Platinum | €80 (€230 − €150) |

Implementado via Stripe como um novo payment intent com o valor diferencial.

## Decisões de Pricing

- **Google Ads apenas no backoffice** (não no convite) — os convidados nunca vêem publicidade; a experiência do convite é sempre limpa
- **Sem downgrade** — não está definido para o MVP
- **Pagamento pré-pago** — sem trial, sem subscrição mensal
- **Retenção Light = D+1** — o evento expira no dia a seguir ao casamento; sem necessidade de guardar dados após o evento para este tier
