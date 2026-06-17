# Secure AI Workshop — Building a Secure Internal AI System for Higher Education

Workshop materials on designing a **secure, internal AI system** for
universities — architecture, governance, and human-in-the-loop design for
institutions moving off public cloud AI.

> 30-minute talk + 30-minute hands-on activity. This repo holds the slides, the
> participant worksheet, and a runnable notebook lab.

---

## 📦 What's inside

| Folder | File | What it is |
|---|---|---|
| [`slides/`](slides/) | `Secure-AI-Workshop-slides.pdf` | The full talk (27 slides, 16:9) |
| [`worksheet/`](worksheet/) | `Secure-AI-Workshop-worksheet.pdf` · `.docx` | Participant worksheet — *"Your Turn: Design a Secure Workflow"* (PDF to print, `.docx` to edit) |
| [`notebooks/`](notebooks/) | `00`–`04` `.ipynb` | Hands-on lab: run the secure pipeline yourself |

## 🧪 Hands-on notebooks — quick start

The notebooks let you *run* the architecture from the talk: PII redaction, RAG
grounding, the 70% confidence threshold, and a tamper-evident audit log.

```bash
git clone https://github.com/tuannguyenvku/secure-ai-higher-ed-workshop
cd secure-ai-higher-ed-workshop/notebooks
pip install notebook        # or: jupyterlab
jupyter lab                 # open 00_Overview, then 01 → 04
```

- **No API key required** — a deterministic mock LLM runs everything offline
  (Python ≥ 3.9, standard library only).
- Each notebook maps to a worksheet step. The last cell of `00` shows how to
  swap in the real Claude client.

| Notebook | Worksheet step | Architecture layer |
|---|---|---|
| `01_Input_Safety_PII` | Step 2 · L3 | PII redaction & injection screening |
| `02_RAG_Grounding` | Step 2 · L4 | Grounding answers in institutional sources |
| `03_Confidence_HITL_Audit` | Step 3 | 70% threshold, the "62% test", audit log |
| `04_Scenario_Lab` | Steps 0–3 | End-to-end pipeline (Scenario A & B) |

## 🔑 The idea in one line

> **Bring AI inside the walls — controlled, grounded, and human-supervised.**
> Confident answers flow through; uncertain ones (below the 70% threshold) pause
> for a human.

## 👤 Author

**Nguyen Thanh Tuan** — Vietnam–Korea University of ICT, The University of Danang
· nttuan@vku.udn.vn

## 📄 License

Slides and worksheet are shared under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) for educational use.
Notebook code is released under the MIT License — reuse and adapt freely with
attribution.
