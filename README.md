# cordoval-models

Public model weights for [Cordoval AI](https://github.com/Gitkierenoffical/Cordoval-AI).  
No application source code and no secrets.

## gemma-router-v2

ONNX q4 tree under `gemma-router-v2/`. Large files are split into ≤15MB parts for
[jsDelivr](https://www.jsdelivr.com/) (20 MB/file limit):

- `onnx/parts/…` + `onnx/model_q4.manifest.json`
- `tokenizer-parts/…` + `tokenizer.manifest.json` (when tokenizer.json > 15 MiB)

The Cordoval app reassembles into Cache Storage / OPFS.

### Licence / attribution

Derived from **Gemma** (Google DeepMind). Subject to the
[Gemma Terms of Use](https://ai.google.dev/gemma/terms).

jsDelivr base (after push + tag `v2`):

```
https://cdn.jsdelivr.net/gh/Gitkierenoffical/cordoval-models@v2/gemma-router-v2
```

Set on the Cordoval deploy:

```
VITE_GEMMA_ROUTER_BASE=https://cdn.jsdelivr.net/gh/Gitkierenoffical/cordoval-models@v2/gemma-router-v2
```

## v2 on-device chat models (GitHub Release `v2-chat`)

Unmodified mirrors of Hugging Face `onnx-community/gemma-3-1b-it-ONNX` (q4) and
`onnx-community/gemma-3-4b-it-ONNX` (q4, text-only: decoder + embed_tokens, no vision encoder).
Each file is verified against Hugging Face's sha256 (LFS) / git blob id. Nothing is split.

Asset name: `<repoPath>--<path with / replaced by -->`, e.g.
`https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-1b-it-q4--onnx--model_q4.onnx_data`

Full list (bytes, sha256, URL): [`manifests/v2-chat-models.json`](manifests/v2-chat-models.json).

| Asset | Bytes |
|---|---|
| [`chat-gemma3-1b-it-q4--config.json`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-1b-it-q4--config.json) | 1,975 |
| [`chat-gemma3-1b-it-q4--generation_config.json`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-1b-it-q4--generation_config.json) | 244 |
| [`chat-gemma3-1b-it-q4--tokenizer.json`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-1b-it-q4--tokenizer.json) | 20,323,013 |
| [`chat-gemma3-1b-it-q4--tokenizer_config.json`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-1b-it-q4--tokenizer_config.json) | 2,327 |
| [`chat-gemma3-1b-it-q4--special_tokens_map.json`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-1b-it-q4--special_tokens_map.json) | 662 |
| [`chat-gemma3-1b-it-q4--chat_template.jinja`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-1b-it-q4--chat_template.jinja) | 1,532 |
| [`chat-gemma3-1b-it-q4--onnx--model_q4.onnx`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-1b-it-q4--onnx--model_q4.onnx) | 347,363 |
| [`chat-gemma3-1b-it-q4--onnx--model_q4.onnx_data`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-1b-it-q4--onnx--model_q4.onnx_data) | 859,106,816 |
| [`chat-gemma3-4b-it-q4--config.json`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-4b-it-q4--config.json) | 3,141 |
| [`chat-gemma3-4b-it-q4--generation_config.json`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-4b-it-q4--generation_config.json) | 244 |
| [`chat-gemma3-4b-it-q4--tokenizer.json`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-4b-it-q4--tokenizer.json) | 20,323,105 |
| [`chat-gemma3-4b-it-q4--tokenizer_config.json`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-4b-it-q4--tokenizer_config.json) | 2,327 |
| [`chat-gemma3-4b-it-q4--chat_template.jinja`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-4b-it-q4--chat_template.jinja) | 1,532 |
| [`chat-gemma3-4b-it-q4--onnx--decoder_model_merged_q4.onnx`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-4b-it-q4--onnx--decoder_model_merged_q4.onnx) | 467,689 |
| [`chat-gemma3-4b-it-q4--onnx--decoder_model_merged_q4.onnx_data`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-4b-it-q4--onnx--decoder_model_merged_q4.onnx_data) | 2,093,692,928 |
| [`chat-gemma3-4b-it-q4--onnx--decoder_model_merged_q4.onnx_data_1`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-4b-it-q4--onnx--decoder_model_merged_q4.onnx_data_1) | 661,772,800 |
| [`chat-gemma3-4b-it-q4--onnx--embed_tokens_q4.onnx`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-4b-it-q4--onnx--embed_tokens_q4.onnx) | 858 |
| [`chat-gemma3-4b-it-q4--onnx--embed_tokens_q4.onnx_data`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-chat/chat-gemma3-4b-it-q4--onnx--embed_tokens_q4.onnx_data) | 430,021,120 |

Licence: Gemma Terms of Use (https://ai.google.dev/gemma/terms).
