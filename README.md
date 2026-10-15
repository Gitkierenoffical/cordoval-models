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
