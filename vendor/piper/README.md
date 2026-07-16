# Vendored: piper-tts-web

In-browser neural TTS (Piper / VITS via onnxruntime-web). Vendored so its blob
workers load same-origin. Only the three dist files are needed:
piper-tts-web.js (entry) + its two chunks.

- Library: @mintplex-labs/piper-tts-web v1.0.4 (MIT) — fork of @diffusion-studio/vits-web
- Voice models: Rhasspy Piper (MIT), fetched at runtime from
  https://huggingface.co/diffusionstudio/piper-voices
- onnxruntime-web (cdnjs) + piper_phonemize wasm (jsdelivr) load at runtime.

App usage: dynamic import('vendor/piper/piper-tts-web.js'); predict({text, voiceId}).
Voices used: de_DE-thorsten-medium, tr_TR-dfki-medium.
