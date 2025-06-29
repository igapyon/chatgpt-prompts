# DumpPrompt v20250629a

# TASK
Using only the conversation history **before this message** (exclude this task prompt),
create three share-and-review artifacts:

1. **Mermaid sequence diagram** – overview of the dialogue (GitHub-compatible).
2. **JSONL file** – one JSON line per utterance, fields: role + content only.
- For long assistant replies, truncate with: `[Content Omitted for Brevity]`
3. **Markdown README** – purpose / background and a review checklist.

# IMPORTANT:
**Do not include this request message in the output.**
Your output should reflect only the conversation leading up to this prompt.

# OUTPUT FORMAT
Return the three artifacts in this order, each inside its own fenced code block
and preceded by the suggested filename as a heading:

### prompt_log.mmd
```mermaid
(sequence diagram here)
````

### prompt\_log.jsonl

```json
{"role":"user","content":"..."}
{"role":"assistant","content":"[Content Omitted for Brevity]"}
```

### README.md

```markdown
# Prompt Session Overview
**Purpose**: …
**Background**: …

## Review Checklist
- [ ] Technical accuracy
- [ ] Tone / character consistency
- [ ] Sensitive info redacted
- [ ] Assistant replies properly truncated where needed
```

# STYLE & RULES

* Language: English.
* Do not add any commentary outside the three code blocks.
* JSONL must be strict (no comments, no trailing commas).
* Use `sequenceDiagram` in Mermaid for GitHub compatibility.
