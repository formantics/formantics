# RetainFormat – Formatting to Semantics for AI

Formantics is a small, focused web app that **converts visual formatting into explicit semantic tags that AI models can reliably understand**.  
Paste rich text from Word, Google Docs, PDFs, email, or the web and Formantics will preserve your formatting, let you assign meanings (like `Question`, `Answer`, `Time`, `Instruction`), and generate **AI‑ready tagged text** without changing the original order.

---

## Why Formantics exists

Most AI prompts throw away visual intent:

- Bold and italics used for emphasis
- Heading hierarchy
- Color‑coded meaning (e.g. red = answer, green = example)
- Alignment and other inline cues

Once pasted into a plain text prompt, that structure disappears and models must guess. **Formantics treats formatting as data** and turns it into clear semantic tags such as:

```text
<Question>What is your opinion?</Question>
<Answer>I think that is a valuable item.</Answer>
```

This makes prompts more robust, auditable, and easier to debug.

---

## Key features

### Rich text input (no formatting loss)

- Paste from **Word, Google Docs, PDFs, email, websites**, etc.
- Preserves:
  - Bold / strong
  - Italic / emphasis
  - Text color (per exact color)
  - Headings (H1–H6)
  - Underline
  - Alignment (e.g. centered headings)
- Uses a **contenteditable** editor so the DOM and inline formatting are preserved.

### Automatic formatting detection

- Analyses the pasted DOM and **only shows formats that actually exist**:
  - Bold, italic, underline
  - Per‑heading level (H1–H6)
  - Unique text colors
  - Alignment changes
- No assumptions: if a format doesn’t appear in your text, it doesn’t appear in the “Detected formatting” list.

### User‑defined semantic tags

For each detected format, you can provide a **semantic tag name**:

- Example mappings:
  - Bold → `Question`
  - Red text → `Answer`
  - Centered H2 → `Heading`
  - Specific color → `Time`
- These tags are then applied wherever that exact formatting appears.


If you’d like to contribute or share feedback, use the **Like / Dislike / Question** buttons in the app or open an issue on GitHub. 
