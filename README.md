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

## v2 speech-to-text voice models (GitHub Release `v2-voice`)

Unmodified files from the sherpa-onnx pack `sherpa-onnx-sense-voice-zh-en-ja-ko-yue-2024-07-17`
(Hugging Face mirror `csukuangfj/...`) and `silero_vad.onnx` from the k2-fsa/sherpa-onnx `asr-models` release.
Details in [`manifests/v2-voice-models.json`](manifests/v2-voice-models.json).

| Asset | Bytes | sha256 |
|---|---|---|
| [`voice-sensevoice-small--model.int8.onnx`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-voice/voice-sensevoice-small--model.int8.onnx) | 239,233,841 | `c71f0ce00bec95b07744e116345e33d8cbbe08cef896382cf907bf4b51a2cd51` |
| [`voice-sensevoice-small--tokens.txt`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-voice/voice-sensevoice-small--tokens.txt) | 315,894 | `f449eb28dc567533d7fa59be34e2abca8784f771850c78a47fb731a31429a1dc` |
| [`voice-sensevoice-small--vad--silero_vad.onnx`](https://github.com/Gitkierenoffical/cordoval-models/releases/download/v2-voice/voice-sensevoice-small--vad--silero_vad.onnx) | 643,854 | `9e2449e1087496d8d4caba907f23e0bd3f78d91fa552479bb9c23ac09cbb1fd6` |

### Licences
- **SenseVoice Small** (FunAudioLLM / Alibaba): FunASR Model Open Source License. See https://github.com/modelscope/FunASR?tab=readme-ov-file#license. Keep the attribution and licence notice when you redistribute.
- **Silero VAD** (snakers4/silero-vad): MIT License, Copyright (c) Silero Team.
