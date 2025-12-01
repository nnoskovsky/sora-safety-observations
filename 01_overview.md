# Overview of Personal Sora Safety Observations

## Background

I am a high school student at a physics–math specialized school affiliated with MIPT. I have been using generative image and video models for several years for creative and personal purposes (e.g., visualizing dreams and abstract ideas).

Because I use these systems intensively, I started to notice patterns in how Sora’s safety filters behave, especially in edge cases involving implied violence or disturbing biological processes.

## Methodology (High-Level)

- I used Sora as a regular user, within the normal product interface.
- I did not use any internal tools, leaked prompts, or reverse-engineered code.
- I explored how safety filters responded when:
  - Prompts contained **explicit, obvious trigger words**.
  - Prompts described **neutral-sounding processes** that, when combined, implied something disturbing.
  - Prompts were **fragmented** into several individually harmless parts that together formed a harmful scenario.
- For cameo, I used **my own face** and body, experimenting with:
  - different lip movements,
  - mismatched audio (e.g., another voice while I silently count),
  - minor variations in lighting and angle.

For each interesting behavior, I wrote down:

- the high-level prompt pattern (never storing it as a copy-paste “recipe”),
- a textual description of the output,
- a hypothesis about why the filter did or did not block it.

I then sent structured reports to OpenAI Support.

## High-Level Findings

1. **Trigger-Word Sensitivity**

   The filters tend to be strict when certain obvious words are present (classic “trigger words” related to violence, blood, etc.). This is good, but it can lead to:

   - false positives (harmless educational or medical contexts),
   - over-reliance on keywords.

2. **Semantic Blind Spots**

   When a scenario is described using abstract or technical language, without explicit trigger words, the filter can miss the **overall pattern** of harm. From a human perspective, the described combination might clearly imply violence or disturbing imagery, but the model may still generate it.

3. **Compositional Prompts**

   Breaking a scenario into several neutral pieces can sometimes bypass filters that mostly look at each piece in isolation. The result may be a video that is emotionally and visually disturbing, even though each sentence of the prompt sounds relatively harmless.

4. **Voice–Identity Mismatch in Cameo**

   When using cameo with my own face, but with audio that clearly belongs to a different speaker (e.g., someone with a very different voice), the model can produce videos where the voice and identity do not align. This creates potential risks for deepfake-like misuse and consent violations.

## Limitations

- All observations are based on a limited, personal sample of prompts and videos.
- The system is under active development; some issues I observed may already be fixed.
- I do not claim full coverage of all safety mechanisms; these are just patterns that appeared repeatedly in my personal experiments.

## Why This Matters

These observations suggest that:

- Safety filters benefit from going beyond keyword detection and towards **deeper semantic understanding** of scenes and processes.
- Compositional and context-aware reasoning is crucial: many harmful scenarios are not obvious from a single word or sentence.
- For cameo features, linking voice and identity in a safer way — or at least clearly signaling when they may not match — is important to reduce the risk of misuse.

The next reports go into two specific areas in more detail:

- Trigger words vs. semantic patterns of violence.
- Voice–identity mismatch in cameo-style videos.
