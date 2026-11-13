# FILM (film_net, estilo "Style") em ONNX — câmera lenta com IA do Baliz Editor

- Modelo: FILM: Frame Interpolation for Large Motion (Reda et al., ECCV 2022), Google Research.
- Pesos: os publicados pelos autores em google-research/frame-interpolation (pretrained_models, film_net/Style),
  licença Apache-2.0 (arquivo LICENSE do repositório, que distribui o código e os modelos pré-treinados).
- Conversão: TorchScript fp32 de jkawamoto/frame-interpolation-pytorch (Apache-2.0; sha256
  5f12cf580f1f027f1086f8806b635f8123cd76895a3425ec9aed9755b569357c) → ONNX opset 17 por
  scripts/models/export_film.py do Baliz-Editor (arquitetura reescrita em scripts/models/film_net.py; só os tensores
  foram lidos). ONNX x PyTorch: erro máximo 1,8e-4.
- Arquivo: film_net.onnx (138 072 141 bytes, sha256 e37568c105de266cab157e403766975c7142b19a852325d52a9fb319e608e073),
  em duas partes (`parte0` + `parte1`, juntar na ordem). Modificado em relação ao original: formato (ONNX).
- Licença: Apache-2.0 (LICENSE-Apache-2.0.txt). Permite uso comercial, redistribuição e derivados.
