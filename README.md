# sora-safety-observations
This project is by no means intended to assist in creating prompts to bypass Sora's AI security; it was created to demonstrate the vulnerabilities of modern generative AI, using Sora as an example.

## Scope

- Focus on **content safety** and **filtering behavior** in video generation.
- Emphasis on:
  - Trigger-word–based filtering vs. semantic understanding of violence.
  - Compositional prompts that look neutral word-by-word but harmful as a whole.
  - Voice–identity mismatch risks in cameo-style generation.
- No explicit prompts, no graphic descriptions, no reproduction of harmful content.

## Contents

- `ethics_and_responsibility.md`  
  My personal principles for responsible safety research with generative models.

- `reports/01_overview.md`  
  Overall methodology and a summary of main findings.

- `reports/02_trigger_words_vs_semantics.md`  
  Observations about how filters can over-focus on individual “trigger words” and under-focus on the full semantic pattern.

- `reports/03_cameo_voice_identity.md`  
  Notes on voice–identity mismatch risks when using cameo features.

## Responsible Disclosure

Whenever I identified a potential safety failure, I:

1. Reproduced it only enough times to confirm that it was not a random glitch.
2. Documented the behavior in text (without sharing or publishing the actual video).
3. Sent a structured report to OpenAI Support, including:
   - a high-level description of the prompt pattern,
   - a description of the output behavior,
   - ideas for how the filter might be improved.

I kept all generated videos private and never shared them publicly. I have an archive of email correspondence and notes which can be provided on request to legitimate safety teams.

## Disclaimer

- This repository is **not** an attack manual.
- All descriptions are intentionally abstract and non-actionable.
- The goal is to help researchers and engineers think about safety holes and patch them, not to teach anyone how to exploit them.
