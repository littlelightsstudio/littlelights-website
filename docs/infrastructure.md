# Infrastructure
**Stand: 24.04.2026**

Übersicht aller Hosting-, Domain- und Server-Setups für Little Lights Studio. Lebende Datei, wird mit jedem Setup-Schritt aktualisiert.

---

## Server: Hetzner Cloud

### Production Server

| Feld | Wert |
|---|---|
| **Provider** | Hetzner Cloud |
| **Server-Name** | `lls-prod-01` |
| **Typ** | CPX32 (4 vCPU AMD, 8 GB RAM, 160 GB SSD) |
| **Standort** | Nuremberg |
| **OS** | Ubuntu 24.04 LTS |
| **IPv4** | `46.224.59.56` |
| **IPv6** | `2a01:4f8:1c18:e9d1::1` |
| **Backups** | aktiviert (täglich, 7 Tage Retention) |
| **Kosten** | ~€16.80/Monat (CPX32 €13.99 + Backups €2.80) |

### Konfiguration

- **Swap:** 4 GB Swap-File unter `/swapfile`, in fstab persistiert
- **Timezone:** Europe/Vienna
- **SSH-Zugriff:** ed25519 Key, User `root`
- **SSH-Keys autorisiert:**
  - miso (lokaler Mac, `~/.ssh/id_ed25519.pub`)
  - Lukas (TODO: Public Key hinzufügen wenn er ihn liefert)

### Hosting-Layer: Coolify

Coolify ist ein selbst gehostetes "Vercel-Equivalent": Auto-Deploy aus GitHub, automatische SSL-Zertifikate, Web-UI für App-Verwaltung.

| Feld | Wert |
|---|---|
| **Coolify-URL** | http://46.224.59.56:8000 (später `https://coolify.littlelights.studio`) |
| **Version** | 4.0.0-beta.474 (installiert 24.04.2026) |
| **Admin-Account** | admin@littlelights.studio |
| **Konfig-Pfad** | `/data/coolify/source/` |

> ⚠ **Wichtig:** Backup der Coolify-Env-Datei (`/data/coolify/source/.env`) ausserhalb des Servers ablegen (Passwort-Manager). Enthält Encryption-Keys, ohne die alle gespeicherten Secrets verloren sind, wenn der Server neu aufgesetzt werden müsste.

### GitHub-Integration

- **GitHub App:** `coolify-lls`
- **App ID:** 3519848
- **Installation ID:** 127497266
- **Verknüpfte Repos:**
  - `littlelightsstudio/littlelights-tools`
  - (später: `littlelightsstudio/littlelights-build` für Hauptseite)

---

## Apps auf dem Server

### littlelights-tools (live)

| Feld | Wert |
|---|---|
| **Repo** | https://github.com/littlelightsstudio/littlelights-tools |
| **Lokaler Clone (miso)** | `~/Documents/.../6. Coding/littlelights.tools/` |
| **Domain** | https://tools.littlelights.studio |
| **Branch** | main |
| **Build Pack** | Nixpacks (Node.js, Auto-Detect) |
| **Port (intern)** | 3000 |
| **Auto-Deploy** | bei jedem Push auf `main` |
| **Health-Check** | `/healthz` → `{"ok":true}` |
| **Status** | Live, Landing-Page rendert, API-Proxies funktional sobald Coolify-Env-Vars sauber gesetzt sind |

**Architektur:** Express-Server mit
- Static-File-Hosting unter `public/` (Tool-HTMLs)
- API-Endpoints unter `/api/claude/*` und `/api/notion/*` (Server-Side-Proxies, damit Keys nie im Browser landen)
- Shared Brand-Tokens in `public/assets/styles.css`

**Workspace-Hinweis:** Das Repo ist absichtlich nicht in Dropbox — `.git/`-Sync zwischen mehreren Macs gibt Konflikte. Geteilter Dropbox-Ordner `03 Tools & Coding/` enthält nur `inbox/` (Drop-Zone) und Onboarding-Doku.

### littlelights-studio (kommende Hauptseite)

Geplant für die Migration der jetzigen statischen `littlelights.studio` Seite. Stack: Next.js 15 + Payload CMS, Repo: `littlelightsstudio/littlelights-build`. Wird auf demselben Server unter Coolify als zweite Application deployed werden.

---

## Domains: easyname

Aktueller Registrar **easyname**. DNS-Zone wird ebenfalls bei easyname verwaltet.

| Domain | Verwendung | DNS-Setup |
|---|---|---|
| `littlelights.studio` | Hauptseite + Subdomains | A-Records für Subdomains zeigen auf Hetzner |
| (weitere TLDs falls vorhanden) | TBD | TBD |

### DNS-Einträge

| Record | Typ | Ziel | Zweck |
|---|---|---|---|
| `tools.littlelights.studio` | A | `46.224.59.56` | Tools-Repo |
| `tools.littlelights.studio` | AAAA | `2a01:4f8:1c18:e9d1::1` | Tools-Repo IPv6 (optional) |
| (TODO: `coolify.littlelights.studio`) | A | `46.224.59.56` | Coolify-Admin auf eigene Subdomain mit SSL |
| (TODO: `littlelights.studio` Apex) | A | TBD | Hauptseite, kommt mit Migration |

### Geplant: Domain-Migration zu Hetzner

Domains sollen perspektivisch zu Hetzner Domains umziehen, um Provider zu konsolidieren (alles in einem Hetzner-Account).

**Ablauf pro Domain (Standard-Transfer):**
1. Bei easyname: Domain-Lock entfernen, Auth-Code (EPP-Code) anfordern
2. Bei Hetzner Domains: Transfer-Auftrag mit Auth-Code starten, 1-Jahres-Renewal-Gebühr zahlen
3. Bestätigungsmail an Owner-Kontakt → bestätigen
4. Wartezeit: 5–7 Tage
5. DNS-Zone bei Hetzner einrichten (oder existierende Records via Zone-Import übernehmen)

**Stolperfallen:**
- Owner-Kontakt-Daten müssen aktuell und erreichbar sein (.studio braucht ICANN-Verifikation)
- Domains die in den letzten 60 Tagen registriert oder transferiert wurden, sind gesperrt
- DNS-TTL vor dem Transfer auf 300s setzen, damit später keine Caching-Probleme entstehen

**Status:** noch nicht gestartet, kann später separat geplant werden.

---

## Letzte Updates

- **24.04.2026:** Hetzner CPX32 angelegt, Coolify installiert, GitHub-Integration `coolify-lls`, Subdomain `tools.littlelights.studio` aktiv.
