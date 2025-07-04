# FullDumpPrompt v20250705a

# TASK
Using only the conversation history **before this message** (exclude this task prompt),
create three share-and-review artifacts:

1. **JSONL file** – one JSON line per utterance, fields: role + content only.
3. **Markdown README** – purpose / background and a review checklist.

# IMPORTANT:
**Do not include this request message in the output.**
Your output should reflect only the conversation leading up to this prompt.

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

## prompt\_log.jsonl

```json
{"role":"user","content":"..."}
{"role":"assistant","content":"[Content Omitted for Brevity]"}
```

# STYLE & RULES

* Language: Japanese.
* JSONL must be strict (no comments, no trailing commas).
