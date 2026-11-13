# SigLIP multilíngue (base, patch16, 256 px) em ONNX — busca visual da Biblioteca do Baliz Editor

- Modelo: SigLIP (Zhai et al., "Sigmoid Loss for Language Image Pre-Training", 2023), Google.
- Pesos: google/siglip-base-patch16-256-multilingual no Hugging Face (publicado pela própria Google), revisão
  `8952a4eafcde3cb7ab46b1dd629b33f8784ca9c6`, `model.safetensors` sha256
  00df88d823790b34a4d2d0047803ffabd47497ae724fd6659b1533dd793255be. Licença declarada no cartão do modelo: apache-2.0.
- Conversão: `scripts/models/export_siglip.py` do Baliz-Editor (transformers 4.46.3 → ONNX opset 17, depois
  quantização dinâmica int8 por canal do onnxruntime). Modificado em relação ao original: formato e precisão (int8).
  - `siglip_image.onnx` (torre de imagem): 101 887 161 bytes, sha256 7e3de74bcacf17ab04441f11366f76e3c795c135c1d99d29fac53ccd5f0188c0; 2 partes.
  - `siglip_text.onnx` (torre de texto): 278 887 062 bytes, sha256 c58c89ce4ca3531763402dac2d6d63fb368c7c43f7ff5a2f9a0b872ede610f7a; 3 partes.
  - `tokenizer.json` (sem alteração, do mesmo repositório): 16 350 281 bytes, sha256 babbf9fed5f505ac6b28fd820b5108ca6882332ce6b921c8d33f8ff69bf841d9.
- Juntar as partes na ordem (`parte0`, `parte1`, …).
- Licença: Apache-2.0 (LICENSE-Apache-2.0.txt). Permite uso comercial, redistribuição e derivados.
