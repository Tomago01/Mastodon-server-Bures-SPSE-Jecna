# Mastodon projekt pro SPŠE Ječná – Samostatně Nasazená Instance

Tento repozitář obsahuje konfiguraci a nastavení pro spuštění vlastní federované sociální sítě pomocí [Mastodon](https://github.com/mastodon/mastodon).  
Projekt je založen na oficiálním Docker deploymentu a obsahuje základní úpravy pro snadné spuštění.

## Co projekt obsahuje

- `docker-compose.yml` pro definici služeb (web, redis, postgres, sidekiq, streaming).
- `.env.production.sample` jako šablonu konfiguračního souboru.
- Skripty pro první spuštění a administraci serveru.

## Jak projekt nasadit

1. **Klonuj repozitář:**
   ```bash
   git clone https://github.com/tvoje-uzivatelske-jmeno/mastodon-server-setup.git
   cd mastodon-server-setup
   ```

2. **Vytvoř konfigurační soubor:**
   ```bash
   cp .env.production.sample .env.production
   ```

3. **Uprav `.env.production` dle svých potřeb (doména, SMTP, databáze).**

4. **Spusť služby:**
   ```bash
   docker-compose build
   docker-compose up -d
   ```

5. **Inicializuj databázi a vytvoř admin účet:**
   ```bash
   docker-compose run --rm web bin/tootctl accounts create admin@example.com --confirmed --role Admin
   ```

6. **(Volitelné) Nastav reverzní proxy (např. Caddy nebo NGINX) a HTTPS certifikáty.**

## Veřejná instance

Pokud je server nasazen, najdeš ho na:  
🌐 [https://buresweb.site](https://buresweb.site)
