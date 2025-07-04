# FullDumpPrompt v20250705a

# TASK
Using only the conversation history **before this message** (exclude this task prompt),
create three share-and-review artifacts:

1. **Mermaid sequence diagram** – overview of the dialogue (GitHub-compatible).
2. **JSONL file** – one JSON line per utterance, fields: role + content only.
- For long assistant replies, truncate with: `[Content Omitted for Brevity]`
- For character style/persona prompts (e.g., instructions that define AI speech patterns or personas), replace content with: `[Persona Setup Omitted for Brevity]`
3. **Markdown README** – purpose / background and a review checklist.

# IMPORTANT:
**Do not include this request message in the output.**
Your output should reflect only the conversation leading up to this prompt.
**Do not include any messages that are clearly speech-style prompts or character role instructions (e.g., with "キャラクター名", "話法", "一人称", "語尾", etc.) in the JSONL log.**: They should be replaced with: `[Persona Setup Omitted for Brevity]`

# OUTPUT FORMAT
Return the three artifacts in this order, each inside its own fenced code block
and preceded by the suggested filename as a heading:

## README.md

```markdown
<!--
⏪ Session Restore Guide
This README, plus prompt_log.mmd and prompt_log.jsonl, constitute a condensed log
of a previous ChatGPT session.

📌 How to use in a new session:
1. Paste these three fenced blocks into the first message.
2. The assistant should treat them as prior conversation history.
3. Unless explicitly asked, do NOT echo the logs back—just continue the dialogue.
-->

# Prompt Session Overview
**Purpose**: …
**Background**: …

## Review Checklist
- [ ] Technical accuracy
- [ ] Tone / character consistency
- [ ] Sensitive info redacted
- [ ] Assistant replies properly truncated where needed
```

## prompt_log.mmd

```mermaid
sequenceDiagram
  participant U as User
  participant A as Assistant
  U->>A: (example)
````

## prompt\_log.jsonl

```json
{"role":"user","content":"..."}
{"role":"assistant","content":"[Content Omitted for Brevity]"}
```

# STYLE & RULES

* Language: Japanese.
* Do not add any commentary outside the three code blocks.
* JSONL must be strict (no comments, no trailing commas).
* Use `sequenceDiagram` in Mermaid for GitHub compatibility.
