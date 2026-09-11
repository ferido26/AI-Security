## Recon

### Recon Goals

- Model and characteristics: Mistral AI, estimated 7B-Instruct v0.3
- RAG present: yes; able to retrieve source document titles/details
- System prompt: not directly retrievable; answers indicate company guidance embedded
- Determinism/temperature: non-deterministic; responses similar with outliers; estimated temp 0.5–1.0
- Context window: present; model referenced prior instructions; context flags present in responses
- Tools/agency: ticket access with review/comment workflow
- Functionality mapping: per RoE
- Rate limits/quotas: observed ~150 requests/min (empirical)
- Input processing: some special chars recognized; Base64 recognized but not decoded/encoded by system


### Recon Probing Prompts (examples)

- Basic capability/identity probes
- System-prompt/instruction probes
- Determinism fingerprinting (repeat prompt)
- Tokenization/edge cases (e.g., `<|>` tokenization, Unicode canary)
- Encoding/obfuscation (Base64 decode request)
- RAG detection (source listing / document IDs)
- Tools/plugins capabilities (list only)
- Moderation probing
- Non-native language (French)
- Chain-of-thought probe
- Context window/limit probes
- Memory recall probe (note recall)
