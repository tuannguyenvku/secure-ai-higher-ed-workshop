# Secure AI Workshop — Hands-On Notebooks

Runnable companion to the participant worksheet **"Your Turn: Design a Secure
Workflow."** You design a secure workflow on paper; these notebooks let you
*run* one. They implement the seven-layer architecture from the talk.

## Notebooks

| # | Notebook | Worksheet step | Layer(s) |
|---|---|---|---|
| 00 | `00_Overview.ipynb` | — | Map + shared mock LLM |
| 01 | `01_Input_Safety_PII.ipynb` | Step 2 · L3 | PII redaction & injection screening |
| 02 | `02_RAG_Grounding.ipynb` | Step 2 · L4 | RAG grounding + citations |
| 03 | `03_Confidence_HITL_Audit.ipynb` | Step 3 | 70% threshold, the 62% test, audit log |
| 04 | `04_Scenario_Lab.ipynb` | Steps 0–3 | End-to-end pipeline (Scenario A & B) |

## Run it

```bash
pip install notebook        # or: jupyter lab
jupyter lab                 # then open 00 → 04 in order
```

- **No API key needed.** A deterministic mock LLM runs everything offline.
- Each notebook ends with an ✏️ *Your turn* cell — edit the config to match the
  design your group wrote on the worksheet.
- The last cell of `00` shows how to swap in the real Claude client
  (`anthropic`, model `claude-opus-4-8`).

## Regenerate

The notebooks are produced from `build_notebooks.py`:

```bash
python build_notebooks.py
```
