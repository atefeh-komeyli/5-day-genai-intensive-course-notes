## 🧠 DAY 1 – Deep Dive into Large Language Models (LLMs) 

---

**Google AI Course - Companion Summary**  
🔗 [Watch the Podcast – Part 1](https://www.youtube.com/watch?v=mQDlCZZsOyo&list=PLqFaTIg4myu8GFXsSEicf6q_ExhfOr5ck)  
🔗 [Watch the Podcast – Part 2](https://www.youtube.com/watch?v=F_hJ2Ey4BNc&list=PLqFaTIg4myu8GFXsSEicf6q_ExhfOr5ck&index=2)

---

### 🔧 Training Process

Large Language Models go through a 3-stage development cycle:

- **Pre-training**  
  Learn general language patterns from massive unlabeled datasets.

- **Fine-tuning**  
  Adapt the model for specific tasks using smaller labeled datasets.

- **RLHF (Reinforcement Learning from Human Feedback)**  
  Models learn from human preferences via a reward model to align better with human expectations.

➡️ **Parameter-Efficient Fine-Tuning (PEFT)** techniques help reduce training costs:
- **Adapters** – Lightweight modules inserted into model layers.
- **LoRA / QLoRA** – Low-Rank Adaptation for minimal parameter updates.
- **Soft Prompting** – Trainable input embeddings without altering model weights.

---

### ✍️ Prompt Engineering Techniques

Prompting is key to getting smart outputs from LLMs. Strategies include:

- **Zero-shot** – Ask directly, no examples.
- **Few-shot / One-shot** – Provide a few guiding examples.
- **Chain-of-Thought (CoT)** – Encourage step-by-step reasoning.
- **Self-consistency** – Sample multiple reasoning paths and choose the best.
- **Tree of Thoughts (ToT)** – Parallel reasoning branches.
- **ReAct** – Mix reasoning and actions (e.g., calling tools).
- **System Prompting** – Set the model's behavior or role.
- **Role Prompting** – Define a persona for style/tone control.
- **Contextual Prompting** – Add background or documents for relevance.
- **Step-back Prompting** – Zoom out to reframe questions.
- **APE (Auto Prompt Engineering)** – Let the model iterate and pick effective prompts.

---

### ⚙️ Sampling & Generation Methods

Controls how the model generates text:

- **Temperature** – Lower = focused & deterministic; higher = diverse & creative.
- **Top-K Sampling** – Pick from top K likely tokens.
- **Top-P (Nucleus)** – Sample from smallest token set with cumulative probability over a threshold.
- **Greedy Search** – Always pick the most probable token (risk: repetitive output).
- **Random Sampling** – More diverse but less coherent.
- **Best-of-n** – Generate several completions and select the best.

---

### 📈 Evolution of Language Models

| Model         | Highlights |
|---------------|------------|
| **GPT-1**      | Intro to generative pre-training + fine-tuning |
| **BERT**       | Encoder-only; excels at classification |
| **GPT-2**      | Strong zero-shot capabilities |
| **GPT-3**      | 175B params; great at few-shot tasks |
| **InstructGPT**| GPT-3 + human feedback for instructions |
| **GPT-3.5/4**  | Improved reasoning, multi-modal support |
| **LaMDA**      | Dialogue-focused by Google |
| **Gopher**     | DeepMind’s large model |
| **PaLM / PaLM 2** | Great for code & reasoning |
| **Gemini**     | Multi-modal, TPU-optimized (Google) |
| **Gemma**      | Lightweight, open-source |
| **LLaMA 3**     | Meta’s powerful open-source family |
| **Mistral**     | Compact and high-performance |
| **O1 Models**   | Transparent and tunable |
| **DeepSeek**    | RL innovations (Group Relative Policy) |

---

### ⚡ Inference Optimization Techniques

Speed up and scale model inference with these tools:

- **Quantization** – Use lower-precision weights to save memory.
- **QAT (Quantization-Aware Training)** – Train with quantization in mind.
- **Distillation** – Smaller models learn from larger ones.
- **Flash Attention** – Faster and more efficient attention computation.
- **Prefix Caching** – Avoid recomputing previous tokens.
- **Speculative Decoding** – Use a smaller model to guess tokens, then validate with a larger model.

---

### 📏 Evaluation Strategies

LLMs are evaluated using a mix of automatic and human methods:

- **Accuracy** – Factual correctness.
- **Helpfulness** – Relevance to user intent.
- **Creativity** – Novel and thoughtful responses.
- **BLEU / ROUGE** – Standard metrics for text generation.
- **Human Feedback** – Manual scoring of responses.
- **LLM-as-a-Judge** – Use another LLM to rate outputs.

---

### 🛠️ LLM Applications

- ✅ Code generation & explanation  
- 🌍 Translation & localization  
- 📝 Summarization  
- 🤖 Chatbots & virtual agents  
- 🧾 Text classification (e.g., spam, sentiment)  
- 🔍 Information retrieval & RAG systems  
- 🎨 Multimodal AI (text + image/audio/video)

---

### ✅ Best Practices

- Write **clear, focused prompts**
- Use **few-shot examples** for guidance
- **Structure output** with formats like JSON or CSV
- Adjust **temperature & sampling** for tone control
- **Log and analyze** prompt-output pairs
- Use **validators** to check structured outputs
- Add **reasoning steps** for complex answers (e.g., CoT)
- Keep iterating and document learnings!

---
