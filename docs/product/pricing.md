# Modelo de Pricing

## Estrutura de Planos

Todos os planos são **pagos por evento**, **pré-pagos no acto de criação do evento**. Sem tier gratuito.

| Feature | Basic €75 | Premium €150 | Ultra €300 |
|---|:---:|:---:|:---:|
| **Retenção do evento** | D+1 (dia após casamento) | 1 ano pós-evento | 1 ano pós-evento |
| Editor visual (zonas editáveis + preview) | ✅ | ✅ | ✅ |
| Templates (3–5) | ✅ | ✅ | ✅ |
| QR code único (partilha geral) | ✅ | ✅ | ✅ |
| Programa do dia | ✅ | ✅ | ✅ |
| Google Ads no backoffice | ✅ | ❌ | ❌ |
| RSVP + restrições alimentares | ❌ | ✅ | ✅ |
| Dashboard de confirmações | ❌ | ✅ | ✅ |
| Sem publicidade | ❌ | ✅ | ✅ |
| QR codes por convidado (personalizados) | ❌ | ✅ | ✅ |
| Export CSV de convidados | ❌ | ✅ | ✅ |
| Múltiplos designs de convite | ❌ | ✅ | ✅ |
| Analytics básico | ❌ | ✅ | ✅ |
| Playlist personalizada | ❌ | ❌ | ✅ |
| Chat do dia / mensagens entre convidados | ❌ | ❌ | ✅ |
| Galeria colaborativa (upload por convidados) | ❌ | ❌ | ✅ |
| Analytics avançado | ❌ | ❌ | ✅ |
| Página de alojamento | ❌ | ❌ | ✅ |
| Domínio personalizado | ❌ | ❌ | ✅ |
| Early access a novas features | ❌ | ❌ | ✅ |

## Upgrades

O upgrade é sempre possível dentro do mesmo evento. O valor cobrado é **a diferença entre planos**:

| De → Para | Valor cobrado |
|---|---|
| Basic → Premium | €75 (€150 − €75) |
| Basic → Ultra | €225 (€300 − €75) |
| Premium → Ultra | €150 (€300 − €150) |

Implementado via Stripe como um novo payment intent com o valor diferencial.

## Decisões de Pricing

- **Google Ads apenas no backoffice do Basic** — os convidados nunca vêem publicidade em nenhum plano; a experiência do convite é sempre limpa
- **Sem downgrade** — não está previsto
- **Pagamento pré-pago** — sem trial, sem subscrição mensal, sem reembolso
- **Retenção Basic = D+1** — o evento expira no dia a seguir ao casamento
- **RSVP disponível a partir do Premium** — o Basic não inclui gestão de confirmações
