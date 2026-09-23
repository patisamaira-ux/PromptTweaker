# PromptTweaker

A single-page tool that demonstrates prompt engineering techniques. Enter one plain prompt, and the app instantly builds three improved versions — with a role/persona, with a few-shot example, and with chain-of-thought reasoning — and shows all four prompts side by side.

## Why this project

Prompt engineering is easier to *see* than to explain. This tool makes the effect of common techniques (role framing, few-shot examples, step-by-step reasoning) visible in one screen, using the same base prompt as the control — no AI call needed to see what each technique actually changes in the prompt text.

## How it works

- Pure client-side app: one `index.html` file, no build step, no backend, no API key, no sign-up.
- On "Compare prompts," it builds 4 prompt variants from your input, entirely in the browser with JavaScript templates:
  1. **Baseline** — your prompt, unchanged
  2. **Role/persona** — prepends an expert-role instruction
  3. **Few-shot** — adds one worked example before your task
  4. **Chain-of-thought** — asks the model to reason through audience/tone/benefit before answering
- Each card shows the exact rewritten prompt text plus a short note on why that technique helps.

## Running it locally

1. Clone this repo.
2. Open `index.html` in any browser (or serve it with any static file server / VS Code Live Server).
3. Type a prompt and click **Compare prompts**.

No installation, dependencies, or accounts required.

## Deploying

This is a static site — deploy it as-is on Vercel, Netlify, GitHub Pages, or any static host. No environment variables or server code needed.

## Tech stack

- HTML, CSS, vanilla JavaScript

## Notes / limitations

- This version compares the *rewritten prompts themselves*, not live AI outputs — it's a teaching tool for what each technique changes, not an API demo.
- To extend it into a full AI-output comparison later, each `build()` function's result could be sent to any LLM API from a backend that holds the key server-side.

## License

MIT — free to use, modify, and submit as coursework.
