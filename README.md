# Mastodon projekt pro SPŠE Ječná

## O projektu

Tento projekt propojuje žáky všech ročníků na škole SPŠE Ječná prostřednictvím federativní platformy Mastodon. Jeho cílem je usnadnit sdílení zkušeností mezi ročníky, pomoci mladším žákům připravit se na následující rok a vytvořit komunitní prostor pro otázky a odpovědi.

## Proč je projekt unikátní?

- První instance Mastodonu přizpůsobená konkrétní škole.
- Důraz na komunitní propojení napříč ročníky.
- Možnost sdílení anonymních dotazů a odpovědí.
- Open-source řešení vhodné i pro jiné školy.

## Použité technologie

- **Mastodon** (Ruby on Rails + React)
- **Docker** pro snadné nasazení
- **PostgreSQL** jako databázový systém
- **Redis** pro background joby
- **Nginx** jako reverzní proxy
- **Let’s Encrypt** pro HTTPS

## Jak projekt spustit

1. Nainstaluj Docker a Docker Compose.
2. Naklonuj repozitář:
   ```bash
   git clone https://github.com/uzivatel/jecna-mastodon.git
   cd jecna-mastodon
