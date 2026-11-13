# baliz-releases
Releases do Baliz Painel (auto-update)

## Baliz Editor (pasta `editor/`)
- `editor/latest.yml` — feed de atualização do app instalado (electron-updater, provedor "generic").
  Escrito por `npm run dist:publish` do repositório Baliz-Editor, sempre DEPOIS de a release
  `editor-v<versão>` (instalador + .blockmap) existir.
- `editor/sfx/efeitos-sonoros-v1.balizpack` — pacote de efeitos sonoros CC0 (Kenney), baixado sob demanda
  pelo app; URL fixada por commit e SHA-256 em `server/baliz/library/sfx_pack.json`.
- Releases `vendor-*` — espelhos de binários de terceiros usados no build (ex.: ffmpeg n7.1 LGPL do BtbN).
- `editor/sfx/efeitos-sonoros-v2.balizpack` — G20: 231 efeitos CC0 (riser, whoosh, transição, risada/reação, humor,
  impacto, glitch; 2–4 variações por som), OpenGameArt; origem e licença por arquivo no manifesto e em
  `editor/LICENCAS-CONTEUDO-G20.md`.
- `editor/musicas/musicas-livres-v1.balizpack` — G20: 20 músicas CC0 (HoliznaCC0 no Free Music Archive e
  OpenGameArt) por clima e BPM.
- `editor/modelos/` — G20: modelos de IA em ONNX (FILM e SigLIP, Apache-2.0) em partes < 100 MB; LEIA-ME e LICENSE
  em cada pasta. URLs presas ao commit e sha256 em `server/baliz/aimodels.json` do Baliz-Editor.
