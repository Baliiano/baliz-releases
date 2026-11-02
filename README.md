# baliz-releases
Releases do Baliz Painel (auto-update)

## Baliz Editor (pasta `editor/`)
- `editor/latest.yml` — feed de atualização do app instalado (electron-updater, provedor "generic").
  Escrito por `npm run dist:publish` do repositório Baliz-Editor, sempre DEPOIS de a release
  `editor-v<versão>` (instalador + .blockmap) existir.
- `editor/sfx/efeitos-sonoros-v1.balizpack` — pacote de efeitos sonoros CC0 (Kenney), baixado sob demanda
  pelo app; URL fixada por commit e SHA-256 em `server/baliz/library/sfx_pack.json`.
- Releases `vendor-*` — espelhos de binários de terceiros usados no build (ex.: ffmpeg n7.1 LGPL do BtbN).
