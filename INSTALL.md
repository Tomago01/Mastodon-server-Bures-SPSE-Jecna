# INSTALL.md – Rychlý průvodce instalací Mastodonu

## Předpoklady

- Server (VPS) s Linuxem
- Docker a Docker Compose
- Doména a přístup ke správě DNS
- SMTP účet pro zasílání e-mailů (např. Mailgun, Google Workspace)

## Instalace

1. **Klonuj repozitář:**
   ```bash
   git clone https://github.com/tvoje-uzivatelske-jmeno/mastodon-server-setup.git
   cd mastodon-server-setup
    ```

2. **Zkopíruj konfigurační šablonu:**

```bash
cp .env.production.sample .env.production
Uprav .env.production podle instrukcí:

LOCAL_DOMAIN, SMTP_SERVER, DB_PASSWORD atd.
```
3. **Postav a spusť kontejnery:**

```bash

docker-compose build
docker-compose up -d
```
4. **Inicializuj databázi a vytvoř admin účet:**

```bash
docker-compose run --rm web bin/tootctl accounts create admin@example.com --confirmed --role Admin
```
5. **Ověř spuštění instance na vlastní doméně (např. https://social.domena.cz).**