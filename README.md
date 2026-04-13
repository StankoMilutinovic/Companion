# Companion — Deployment na Vercel

## Šta imaš
- `index.html` — kompletan app (onboarding, chat, SOS, sve oblasti)
- `vercel.json` — Vercel konfiguracija

## Koraci (10-15 minuta)

### 1. GitHub (besplatno)
1. Idi na github.com → prijavi se ili kreiraj nalog
2. Klikni "New repository" → nazovi ga "companion"
3. Uploaduj oba fajla (index.html i vercel.json)

### 2. Vercel (besplatno)
1. Idi na vercel.com → "Sign up with GitHub"
2. Klikni "Add New Project"
3. Izaberi "companion" repo
4. Klikni "Deploy" — gotovo

### 3. API Key (VAŽNO)
App poziva Anthropic API direktno iz browsera.
Za produkciju trebaš backend proxy (da sakriješ API key).

Za testiranje lokalno:
- Otvori index.html u browseru
- Dodaj API key direktno u kod (privremeno, samo za test):
  Pronađi `headers: { 'Content-Type': 'application/json' }`
  Dodaj: `'x-api-key': 'tvoj-api-key', 'anthropic-version': '2023-06-01'`

Za produkciju (siguran način):
- Napravi Vercel Serverless Function kao proxy
- Javi se — dam ti kompletan kod za to (30 minuta)

## Lokalni test
Samo otvori index.html u Chrome/Firefox.
Onboarding i UI rade bez API-ja.
Chat zahtijeva API key.

## Domen
Na Vercelu dobijaš: companion-xyz.vercel.app
Za companion.rs — kupi domen i poveži u Vercel dashboard.
