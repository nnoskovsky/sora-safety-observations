# Trigger Words vs. Semantic Patterns of Harm

## 1. Observation

In my personal experiments, Sora’s safety behavior often seemed strongly influenced by the presence or absence of specific “trigger words” in the prompt text. When those words appeared explicitly, the filter was usually strict and blocked generations.

However, when I described scenarios using:

- abstract terminology,
- neutral or technical language,
- fragmented descriptions of processes,

the system sometimes allowed outputs that, from a human perspective, clearly belonged to a disturbing or harmful category.

I do **not** include the actual prompts here. Instead, I summarize the patterns.

## 2. Categories of Prompts

### 2.1 Direct, Explicit Prompts

- Contain obvious terms associated with violence or graphic harm.
- The filter generally recognizes and blocks these.
- Good for basic safety, but limited.

### 2.2 Abstract Process Descriptions

- Use neutral words describing biological or physical processes.
- When those processes are mentally combined, they imply something unsettling.
- The filter sometimes appears to treat each part as harmless, missing the global meaning.

### 2.3 Fragmented Compositional Prompts

- The harmful meaning emerges only when multiple lines are mentally combined.
- Each individual sentence looks safe in isolation.
- A human reader, reading the entire prompt, would likely recognize a disturbing pattern; the filter sometimes does not.

## 3. Why This Is a Problem

Humans do not only react to keywords; we react to **context, intent, and composition**. A system that relies heavily on trigger words can:

- Block harmless content that uses certain words in an educational or medical context.
- Allow harmful or disturbing content that is carefully phrased in abstract or technical terms.

This creates a gap between human expectations of safety and the actual behavior of the filter.

## 4. High-Level Ideas for Improvement

These are conceptual suggestions, not implementation details:

- **Semantic scene understanding**  
  Go beyond scanning for individual words and analyze the combined meaning of entities, actions, and processes described in the prompt.

- **Compositional risk scoring**  
  Instead of assessing each sentence separately, compute a risk score based on how multiple sentences combine into a single narrative.

- **Pattern recognition over time**  
  Some prompts describe multi-step processes; understanding the temporal and causal connections between steps can reveal hidden harm.

- **Context-sensitive thresholds**  
  Consider different safety thresholds for obviously fictional horror vs. realistic or instructional content, while still avoiding graphic harm.

## 5. Responsible Framing

The goal of documenting these patterns is to:

- Help safety teams think about where trigger-word–based filters are strong or weak.
- Encourage more semantic and context-aware approaches.
- Avoid giving anyone enough detail to reliably reproduce harmful prompts.

For that reason, I avoid including concrete examples, and I recommend that anyone doing similar research follow the same principle in public.
