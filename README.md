<p align="center">
  <img src="assets/avatar.png" width="96" height="96" alt="Fixplay">
</p>

# Fixplay

Reparaturplattform für Smartphones und Konsolen aus Königslutter am Elm.

Fixplay verbindet die Werkstatt mit Kunden, Partnern und dem eigenen
Werkstatt-Alltag: Reparaturannahme, Refurbished-Shop, Partner-Sourcing und
Hardware-Diagnose — von der öffentlichen Website bis zum Etikettendrucker.

- **Website:** [fixplay.de](https://fixplay.de)
- **Partner-Portal:** [partners.fixplay.de](https://partners.fixplay.de)

## Repositories

| Repository | Zweck |
|---|---|
| [`fixplay-backend`](https://github.com/fixplay-orga/fixplay-backend) | Go-Backend: Public API (`:7000`, Firebase JWT) und Admin API (`:7100`, Basic Auth) |
| [`fixplay-frontend`](https://github.com/fixplay-orga/fixplay-frontend) | Kundenshop und Reparaturplattform (Nuxt 4, Nitro-BFF, OpenAPI-Contract) |
| [`fixplay-frontend-admin`](https://github.com/fixplay-orga/fixplay-frontend-admin) | Admin-Dashboard im Browser und als Android-App (Vue 3, PrimeVue, Capacitor) |
| [`fixplay-frontend-partners`](https://github.com/fixplay-orga/fixplay-frontend-partners) | Partner-Portal für Sucher und Vertrieb (Vue 3, Firebase Auth) |
| [`fixplay-diagnoseTool`](https://github.com/fixplay-orga/fixplay-diagnoseTool) | Desktop-Tool für NOR-Flash, UART- und Controller-Diagnose (Tauri v2) |
| [`ql700-printserver`](https://github.com/fixplay-orga/ql700-printserver) | Etikettendruck-Server für den Brother QL-700 |

Archiviert: [`fixplay-frontend-legacy`](https://github.com/fixplay-orga/fixplay-frontend-legacy)
(Vue-3-Kundenshop) und [`fixplay-backend-legacy`](https://github.com/fixplay-orga/fixplay-backend-legacy)
(Java/Javalin-Backend).

## Arbeitsweise

- **Contract-first:** Das Go-Backend veröffentlicht `openapi-public.yaml` als
  Release-Asset; Frontends pinnen Version und SHA256 statt eine Spec von Hand
  zu pflegen.
- **Getrennte Oberflächen:** Kunden-, Admin- und Partner-Portal haben eigene
  APIs, Auth-Verfahren und Deployments. Interne Bereiche sind nie öffentlich
  verlinkt; fehlende Rechte führen bewusst auf 404 statt 403.
- **Testbar ohne Hardware:** Rust-Hardwarezugriffe laufen hinter Traits mit
  Mock-Implementierungen; die Frontends haben Vitest-Suiten, MSW-Mocks und
  Docker-Rezepte für reproduzierbare Builds.
- **Deutsch als Produktsprache**, Code, Kommentare und Commits auf Englisch —
  mit deutschen Fachbegriffen dort, wo sie eindeutiger sind.

## Sicherheit

Bitte Schwachstellen nicht als öffentliches Issue melden, sondern vertraulich
an den Repository-Owner. Details stehen in `SECURITY.md` des jeweiligen
Repositories.
