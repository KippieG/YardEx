# YardEx — Havenruimte Beurs Zeebrugge

Anoniem B2B platform waar Zeebrugse terminals overtollige yard-ruimte en slots aan elkaar verhuren.

## Stack

- **Server:** Node.js + Express + PostgreSQL
- **Client:** React + Vite + CSS variabelen
- **Auth:** JWT (7 dagen geldig)
- **DB:** PostgreSQL met UUID primary keys

## Lokaal starten

### 1. Database opzetten

```bash
createdb yardex
psql yardex < database/migrations/001_init.sql
```

### 2. Server

```bash
cd server
cp .env.example .env
# Pas .env aan met jouw DB-credentials
npm install
npm run dev
```

### 3. Client

```bash
cd client
npm install
npm run dev
```

App draait op http://localhost:5173

## Features (MVP)

- **Anonieme marktplaats** — bedrijven zien enkel alias, nooit echte naam of e-mail
- **Listings** — terrein (m²), truck-slots, vessel-slots met datum en prijs
- **Aanvragen** — anoniem aanvragen indienen met geboden prijs
- **Deals** — accept/reject flow met automatische deal-aanmaak
- **Notificaties** — realtime updates voor nieuwe listings en aanvragen
- **Dashboard** — overzicht van actieve capaciteit, openstaande deals en inkomsten

## Businessmodel

- **Transactiecommissie:** 2–4% per gematcht deal
- **Maandabonnement:** analytics dashboard per terminal
- **API-integratie:** koppeling met TOS (Navis N4, CargoWise)

## Roadmap

- [ ] E-mail notificaties (SendGrid)
- [ ] AI prijssuggester op basis van historische havendata
- [ ] TOS-integratie (Navis N4 API)
- [ ] Stripe transactieverwerking
- [ ] Uitrol naar Antwerpen
