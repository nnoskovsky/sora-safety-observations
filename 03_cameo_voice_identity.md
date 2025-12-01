# Cameo, Voice, and Identity Mismatch

## 1. Background

Sora’s cameo feature allows users to insert themselves (their face and body) into generated video scenes. This is a powerful and creative tool, but it also raises important safety and consent questions.

In my personal experiments, I used only my own appearance. I was curious how the model would handle situations where the **visual identity** and the **audio voice** do not belong to the same person.

## 2. Key Observation

When I:

- used my own cameo (face and body),
- moved my lips in simple patterns (for example, silently counting numbers),
- combined this with audio that clearly belonged to another speaker,

the generated video sometimes looked like:

- “me” speaking with someone else’s voice,
- with lip movements that roughly matched the rhythm but not the true speech.

From the viewer’s perspective, it can appear as if I am saying words that I never actually said, with a voice that is not mine.

## 3. Risks

This type of mismatch can be exploited for:

- Deepfake-like content where a person appears to say something they never said.
- Misleading or malicious videos that damage reputations or violate consent.
- Confusion about who is responsible for the voice and message in the video.

Even if the system is not designed as a deepfake tool, the combination of cameo and flexible audio can create similar risks.

## 4. High-Level Ideas for Mitigation

Again, these are conceptual ideas, not implementation details:

- **Stronger linkage between identity and voice**  
  Allow users to explicitly opt into linking their own recorded voice with their visual cameo, and clearly distinguish this from synthetic or third-party voices.

- **Clear labeling**  
  Add visual or metadata indicators when:
  - the voice is synthetic,
  - the voice and face are unlikely to belong to the same person.

- **Stricter policies on third-party voices**  
  Limit or monitor scenarios where a user tries to combine a cameo of one person with audio that obviously belongs to a different, recognizable person.

- **Detection and internal alarms**  
  Develop internal systems that flag content where lip movements and voice characteristics are strongly mismatched, especially for realistic, non-fantasy scenes.

## 5. Personal Responsibility

In all experiments:

- I only used my own face in cameo.
- I did not share any generated videos publicly.
- I reported my observations to OpenAI Support with a focus on potential misuse and consent issues.

I believe it is important that powerful video generation tools adopt strong safeguards against deepfake-like misuse, especially as they become more widely available.
