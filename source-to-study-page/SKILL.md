---
name: source-to-study-page
description: Transform given material into self-contained Tailwind-styled educational HTML study pages.
---

# Source to study page

Turn supplied reference material into one offline HTML page that helps a university student understand and review it. Treat the reference as authoritative. The page may clarify, organize, and teach the source, but it must not silently add facts.

Read [references/educational-html-spec.md](references/educational-html-spec.md) before building the page. It defines the page structure, visual requirements, accessibility, and interactions.

## 1. Inspect the input

- Do not browse for supporting facts unless the user explicitly requests outside research. A missing explanation is better than an invented one.
- For PDFs, extract the text and inspect rendered pages when layout, tables, formulas, figures, footnotes, or scan quality affect meaning. Use OCR only when it is available and check the result against the page image.
- For text files, preserve headings, lists, code, formulas, tables, quotations, and explicit qualifiers.

## 2. Build a source ledger before writing

Create an internal ledger that maps each planned factual claim, definition, example, number, formula, quotation, and learning objective to a source location.

- Cite PDF claims by page number. Cite text claims by heading, section, or paragraph when page numbers do not exist.
- Keep definitions and qualifiers intact. Do not turn a possibility into a certainty, a correlation into a cause, or a source limitation into a conclusion.
- If sources disagree, preserve the disagreement and cite both locations. Do not merge conflicting claims or choose a winner without source support.
- Separate source content from teaching additions. Label a paraphrase as a paraphrase when needed. Use source-provided examples by default. Any new analogy or hypothetical example must be clearly labeled and must not be presented as evidence from the source.

## 3. Design the lesson

- Target university students unless the user gives a different audience.

- Explain source terminology in plain language, keep the source's technical precision, and introduce prerequisites only when the source supports them or the page clearly labels them as outside context.

- Use concise paraphrasing over source-like wording: shorten and simplify explanations wherever possible to improve intuition and engagement, while preserving the source's meaning, qualifiers, and technical precision.


Include the learning elements in the reference spec:

- a concise title, source list, scope, and limits
- learning objectives derived from the source
- a short overview and a logical progression of key ideas
- key terms and definitions
- source-grounded worked examples, figures, tables, or formulas when useful
- retrieval questions and a short quiz with answer explanations
- a compact takeaway section and source notes

Questions must test what the source teaches. Do not add trick questions or require outside knowledge. If the source does not cover a requested point, say so in the page instead of filling the gap.



## 5. Build one offline HTML file

- Use Tailwind CSS utility classes and compile the required CSS at build time
- Embed source figures when they improve understanding and can be extracted reliably.
- Use semantic HTML, a clear heading hierarchy, readable line length, responsive layout, visible keyboard focus, sufficient contrast, a skip link, and controls that work without color alone.
- Use lightweight inline JavaScript only for useful local interactions such as showing answers, checking quiz responses, filtering sections, or updating progress. The lesson must remain readable if JavaScript is disabled.

## 5. Verify before delivery

- Recheck every factual block against the source ledger. Remove unsupported claims, decorative filler, and invented context.
- Confirm that citations point to real pages or sections and that source notes identify the input files.
- Check that all internal navigation links work, answer controls reveal the correct explanation, quiz scoring handles unanswered items.
