# UVic AI Learning Lab - Student Guide

**SENG480B / CSC586C | Fall 2026**

The UVic AI Learning Lab is the university's own AI platform, hosted on UVic teaching computing infrastructure. It gives you a chat interface, Jupyter notebooks, and an OpenAI-compatible API, all running on models served inside the university. Nothing you send leaves UVic. This is the AI environment for all course work in this class.

---

## 1. Terms of Use

By using the AI Learning Lab you agree to the following:

- **Acceptable use.** No NSFW, hateful, harassing, insulting, racist, or discriminatory content. No attempts to break, overload, or bypass the platform. UVic's IT acceptable use policies apply.
- **⚠️ All prompts are logged.** Every message you send and every response you receive is logged by the university. Logs are actively monitored, and **UVic IT staff will review them**.
- **No expectation of privacy.** Treat every chat as visible to staff. The one guarantee: all data stays within the university and is not sent to any outside provider.
- **Don't share others' personal data.** Do not paste personal or confidential information about other people (classmates, clients, users) into prompts.
- **Your key is yours alone.** Sharing API keys is strictly prohibited. Do not post it in chat, Slack, or commit it to Git. Shared or leaked keys will be revoked.
- **Rate Limitation.** 2 max-parallel-requests per key, 60 request per minute (pooled)
- **Access ends:**
  - at the end of the term, and
  - immediately if you drop the course.
- **Academic integrity.** Follow the course policy on disclosing AI use in your submissions.

---

## 2. Overview

### Models

| Model | What it's for | Context | Max output | Tools | Vision | Reasoning |
|---|---|---|---|---|---|---|
| `qwen3-6-35b-a3b-vllm` **(default)** | Code generation and explanation, agent tasks, screenshots and diagrams | 87,500 tokens | 10,304 tokens | Yes | Yes | Yes |
| `ministral-3-3b-cpu` | Code completion, quick chat, summaries | 112,000 tokens | 16,000 tokens | Yes | No | No |
| `chandra-ocr-2-vllm` | OCR: turns images and scanned documents into text | 20,480 tokens | 12,384 tokens | No | Yes | No |

**`qwen3-6-35b-a3b-vllm` is the default model for code generation and explanation.** It is Qwen3.6-35B-A3B, a mixture-of-experts model (35B parameters total, about 3B active per token) served on GPU with vLLM. It supports tool calling, image input (screenshots, UI mockups, diagrams), and reasoning, meaning it "thinks" before answering. That thinking uses part of the 10k output budget, so very long answers may get cut off. Use it for anything code related.

**`ministral-3-3b-cpu`** is a small (3B parameter) Mistral model running on CPU. It is a task model for things like auto-complete for coding. Configure auto-completion on your client. It handles text only, with a large 112k context window (roughly 80k words), but it is slower and less capable than Qwen. Use it for light tasks or as a fallback when Qwen is busy.

**`chandra-ocr-2-vllm`** reads images and scanned pages (handwriting, tables, forms, math) and returns structured text. **Max image size: 6,291,456 pixels (about 2508 x 2508).** 

### Services

| Service | URL | What it is |
|---|---|---|
| Web chat | https://chat-ai.uvic.ca/ | Browser chat interface (Open WebUI). Pick a model and start talking. Easiest place to start. |
| JupyterHub | https://jhub-ai.uvic.ca/ | Your own Python notebook environment in the browser. Good for scripting against the API, testing prompts, and data work. |
| OpenAI-compatible API | `https://api-ailearninglab-prod.uvic.ca/v1/` | Programmatic access for code, IDE extensions, and terminal tools. Works with any OpenAI-compatible library or client. |

---

## 3. Authentication

All services are **only reachable over the UVic VPN**, on or off campus.

**Step 1: Connect to the VPN**

1. Install **Cisco Secure Client** (available from UVic Systems if you don't have it).
2. Enter the VPN address: **`vpn.uvic.ca/seng-ai`**
3. Log in with your **NetLink ID** and **password**.
4. **Check your phone.** A Duo push is sent, but **nothing will show on your computer screen** to tell you. Approve the push on your phone and the VPN connects.

> Duo must be your **default** 2FA method. If it isn't, set it at UVic's 2FA settings page before trying. Without it, login will hang or fail.

**Step 2: Open a service**

Once the VPN is connected, open the web chat or JupyterHub and log in with **UVic SSO** (NetLink ID). The API uses your API key instead (below).

---

## 4. API Setup

Your connection details:

```
Base URL : https://api-ailearninglab-prod.uvic.ca/v1/
API Key  : <YOUR-API-KEY-HERE>
Model    : qwen3-6-35b-a3b-vllm   (default)
```

> The VPN must be connected for the API to work. If a client adds `/v1` on its own and you get 404 errors, use the base URL without `/v1`.

**Quick test (terminal)**

```bash
curl https://api-ailearninglab-prod.uvic.ca/v1/models \
  -H "Authorization: Bearer $AILAB_API_KEY"
```

**Python (OpenAI library)**

```python
import os
from openai import OpenAI

client = OpenAI(base_url="https://api-ailearninglab-prod.uvic.ca/v1/",
                api_key=os.environ["AILAB_API_KEY"])
r = client.chat.completions.create(model="qwen3-6-35b-a3b-vllm",
      messages=[{"role": "user", "content": "Hello!"}])
print(r.choices[0].message.content)
```

Store your key in an environment variable (`AILAB_API_KEY`), never in code.

### Client examples

- **Cline (VS Code extension):** Install **Cline** from the VS Code Extensions marketplace. In Cline settings → API Provider: **OpenAI Compatible** → paste Base URL and API Key → Model ID `qwen3-6-35b-a3b-vllm`. Set context window to `87500`, enable image support, and keep max output tokens at or below `10304`, **not** near the context limit.
- **GitHub Copilot + LiteLLM provider extension (VS Code):** Install the LiteLLM provider extension for Copilot Chat, enter the Base URL and API Key when prompted, then choose `qwen3-6-35b-a3b-vllm` from the Copilot Chat model picker.
- **Terminal clients:** Any OpenAI-compatible CLI works, e.g. **opencode**. Add a custom OpenAI-compatible provider with the same Base URL, key, and model name.

---

## 5. What to Expect

These are open models running on UVic hardware, not commercial services like ChatGPT, Claude, or Gemini. Qwen is a capable coding model, but it is not at the frontier level, so expect some differences in speed and depth. In exchange, your data never leaves the university. **UVic requires that assignment-related work is done with these models, not outside AI services.**

**Managing context**

- Bigger input = slower, and models start forgetting or mixing up details well before their context limit (87.5k for Qwen).
- Start a **new chat** for each new task. Long chats carry old baggage.
- Give only the files and snippets that matter, not the whole repo.
- Be specific: state the goal, the constraints, and the output format you want.
- In agent clients, a high max-output setting eats into the input space and causes silent failures. Keep it low.

**What works well**

- Explaining code, errors, and concepts
- Writing and changing code, focused features, boilerplate
- Reading screenshots of UIs, errors, and diagrams (Qwen)
- Summarizing, rewording, drafting docs and tests
- OCR on clean scans and screenshots (`chandra-ocr-2`)

**What may struggle or fail**

- Large multi-file refactors or long agent runs (the model can loop, stall, or stop mid-task)
- Complex reasoning and architecture decisions
- Responses can be slow, especially when the class is busy (e.g. right before deadlines). Plan ahead.
- Confident but wrong answers. **Always review and test the output.**
- Images sent to `ministral-3-3b-cpu` (text only), or images above the OCR size limit

---

## 6. Troubleshooting

| Problem | Try this |
|---|---|
| VPN login hangs | Check your phone for the Duo push. Confirm Duo is your default 2FA. |
| Site or API won't load | Make sure the VPN is connected to `vpn.uvic.ca/seng-ai`. |
| `401 Unauthorized` | Check the API key, no extra spaces. |
| `404 Not Found` | Try the base URL with or without `/v1`. Check the model name spelling. |
| Empty or cut-off replies | Reduce input size or lower max output tokens. Start a new chat. With Qwen, long reasoning can use up the output budget; lower/disable thinking mode, ask for a shorter answer or split the task. |
| Timeouts | Server is busy. Retry in a few minutes with a shorter prompt. |

---

## 7. Help

Contact the TA, **Bachan Ghimire**, at **bachan48@uvic.ca** or on **Slack**. Include what you tried, which service or client, and the exact error message.
