# OBSIDIAN.SYS // setup

passos manuais necessários pro README funcionar 100%.

## 1. Snake animation (.github/workflows/snake.yml)

já criado. ele vai rodar a cada 12h e gerar 3 SVGs na branch `output`:
- `snake.svg` — light
- `snake-dark.svg` — dark
- `snake-crimson.svg` — paleta obsidian (preto + crimson)

**ação necessária:** ir em `Settings → Actions → General → Workflow permissions` e marcar **"Read and write permissions"**. depois roda o workflow manualmente uma vez (`Actions → generate snake → Run workflow`).

## 2. Spotify "wiretap" (now playing)

o badge no README aponta pra `https://spotify-recently-played-readme.vercel.app`. esse serviço público funciona com qualquer perfil **público** do Spotify — só substituir `SPOTIFY_USER_ID` pelo seu ID.

**como achar seu ID:**
1. abre Spotify desktop, clica no seu perfil
2. `...` → Compartilhar → Copiar link do perfil
3. URL fica `open.spotify.com/user/SEU_ID` — pega o `SEU_ID`

**substituir no README:**
- linha com `SPOTIFY_USER_ID` → seu ID real

**alternativa (mais robusta, mostra now playing real-time):** fork do [novatorem](https://github.com/novatorem/novatorem), deploy próprio na Vercel, secrets `SPOTIFY_CLIENT_ID` / `SPOTIFY_CLIENT_SECRET` / `SPOTIFY_REFRESH_TOKEN`.

## 3. WakaTime stats

precisa de conta no [wakatime.com](https://wakatime.com) + plugin instalado no VS Code. depois:

1. login no WakaTime
2. `Settings → Account` → marcar "Display code time publicly"
3. `Settings → Account` → marcar "Display languages, editors, os, categories publicly"
4. o badge no README usa seu username do WakaTime — substituir `WAKATIME_USER` no README

sem isso o card vai aparecer vazio mas não quebra.

## 4. Pinned repos

os 4 cards de "DEPLOYED_ASSETS" precisam dos nomes reais dos repos. substituir no README:
- `REPO_AGENDAPRO` → nome do repo do AgendaPRO
- `REPO_BUFFALO` → repo do site da Buffalo
- `REPO_HEROES` → repo do Heroes Dogueria
- `REPO_GARAGEM` → repo da Garagem 85

se algum repo for privado, troca por outro público ou remove o card.

## 5. Links de contato (ENCRYPTED_CHANNELS)

substituir no README:
- `LINKEDIN_URL` → URL do seu LinkedIn
- `EMAIL` → seu email (ou usar mailto:)
- `WHATSAPP_URL` → wa.me/55SEU_NUMERO
