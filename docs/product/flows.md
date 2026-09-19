# User Flows — MVP

Scope: Basic + Premium tiers only. Ultra is Fase 2.

---

## Flow 1 — Signup & Plan Selection

```
Landing page
  → CTA "Criar o meu convite"
  → Signup (email + password)
  → Escolha de plano: Basic €75 / Premium €150
  → Detalhes do evento (nomes do casal, data, local)
  → Pagamento Stripe (upfront, one-time)
  → Dashboard / Backoffice
```

---

## Flow 2 — Invitation Builder

```
Backoffice → "Editar convite"
  → Escolha de template
      Basic: selecção limitada (3–5 templates)
      Premium: todos os templates disponíveis
  → Editor de zonas editáveis
      - Nomes do casal
      - Data e hora
      - Local / morada
      - Foto de capa
      - Esquema de cores
      - Mensagem personalizada
  → Preview em tempo real (mobile + desktop)
  → Guardar & Publicar
  → Link público gerado: plataforma.pt/convite/[slug]
  → QR code gerado e disponível para download
```

---

## Flow 3 — Backoffice / Event Management

```
Dashboard
  → Overview do evento (dias para o casamento, nº confirmações, nº visualizações)
  → Editar convite (→ Flow 2)
  → Gestão de convidados
      Basic: lista limitada
      Premium: lista completa, export CSV, QR codes individuais
  → RSVPs (Premium only)
      - Lista de confirmações
      - Restrições alimentares
      - +1s
  → Analytics (Premium only)
      - Visualizações do convite
      - Taxa de RSVP
      - Contagem de confirmações
  → QR code — download / partilha
  → Upgrade de plano (apenas se Basic) (→ Flow 5)
  → Referral (→ Flow 6)
  → Definições de conta
```

---

## Flow 4 — Guest Invitation View (público)

```
Convidado abre link ou lê QR code
  → plataforma.pt/convite/[slug]
  → Visualização do convite (estilizado, sem branding da plataforma no Premium)
  → Formulário de RSVP (apenas Premium)
      - Nome
      - Presença (confirma / não confirma)
      - Restrições alimentares
      - +1
  → Confirmação de submissão
```

Nota: convidados nunca vêem publicidade em nenhum plano.

---

## Flow 5 — Upgrade Flow

```
Backoffice → CTA "Upgrade para Premium"
  → Comparação de features (Basic vs Premium)
  → Confirmação do valor a pagar: €75 (diferença)
  → Stripe checkout (novo payment intent com valor diferencial)
  → Webhook Stripe confirma pagamento
  → Backoffice actualizado com features Premium desbloqueadas
```

---

## Flow 6 — Referral

```
Backoffice → "Convidar um casal"
  → Link de referral único gerado
  → Casal partilha o link
  → Novo utilizador abre link → €10 de desconto aplicado automaticamente no checkout
  → Após pagamento do novo utilizador:
      → Referrer recebe €15 de crédito para upgrade de plano
      → Crédito visível no backoffice
```

---

## Decisões Fechadas

| Decisão | Escolha |
|---|---|
| Autenticação | Email + password tradicional (MVP) |
| URL do convite público | Path-based: `plataforma.pt/convite/[slug]` |
| Subdomínio por casal | Não — Fase 2 / Ultra |
