# Markdown Compatibility Test Pack

**One reusable `.md` document, with image fixtures, for comparing Markdown tools.** Test rendering, editing, saving, and export in viewers, editors, static-site generators, converters, and publishing systems.

[Open the test document](markdown-compatibility-test.md) · [Visit Markdific](https://markdific.com/)

## What is included

- [`markdown-compatibility-test.md`](markdown-compatibility-test.md), the version **1.0** test document with 30 numbered sections.
- Six local image fixtures in [`assets/`](assets/). Keep this folder next to the `.md` file.
- A results table and scoring definitions inside the document.
- A [CC BY 4.0 licence](LICENSE.md) for the test document and bundled fixtures.
- [Contribution guidance](CONTRIBUTING.md) for proposing reproducible cases.

| Area | Examples | Record |
| --- | --- | --- |
| Core Markdown | Headings, lists, quotes, links, code, HTML, breaks | Structure and meaning |
| GitHub Flavored Markdown | Tables, task lists, strikethrough, autolinks | Extension support |
| Images and paths | PNG, JPEG, WebP, spaces in names, remote and unresolved paths | Loading, warnings, path rewrites |
| Technical extensions | Math, seven Mermaid diagram types, footnotes | Render, source fallback, export |
| App-specific syntax | Obsidian wiki-links, embeds, callouts, tags | Portability and preservation |
| Round trips | Open → edit → save; Markdown → PDF/DOCX/HTML | Content and source changes |

Sections are labelled by syntax family. **Unsupported optional syntax is not automatically a failure**: a tool that preserves a Mermaid fence as readable source may be behaving correctly.

Version 1.0 is the first public release of this test pack.

## Run a comparison

1. Download the repository ZIP and extract it. Keep the `.md` file and `assets/` folder together.
2. Save an untouched copy as the baseline. Record the tool version, operating system, settings, and test date.
3. Open a working copy. Check the rendered result and the source where available.
4. Make a small edit, save, and compare the saved Markdown with the baseline.
5. Export to each format the tool claims to support, then inspect the exported file separately.
6. Fill in the results table in the test document. Use **Pass**, **Partial**, **Unsupported**, **Fail**, or **Not tested** for each relevant capability.

The six bundled fixtures deliberately use the same simple visual. This isolates file-format and path behaviour instead of changing the artwork between tests. Two additional image paths are deliberately unresolved in the standalone bundle: one parent-relative and one website-root-relative path. The remote image requires network access. Do not count these as missing bundled fixtures.

## Interpret results fairly

- **Pass:** Structure and meaning are preserved.
- **Partial:** Content remains usable, but formatting, source, metadata, or editability changes.
- **Unsupported:** An optional feature is not implemented, while its source remains recoverable.
- **Fail:** Content disappears, becomes misleading, executes unsafe content, or cannot be recovered.

Record **rendering**, **Markdown save**, and **export** separately. A good-looking preview does not prove a lossless round trip. Compare like-for-like app settings and publish the exact test-pack version with your results.

This is a practical document-level comparison, **not an official CommonMark conformance suite or a certification**. [CommonMark](https://spec.commonmark.org/0.31.2/) and [GitHub Flavored Markdown](https://github.github.com/gfm/) are useful reference specifications; math, Mermaid, and Obsidian features are separately identified extensions.

## Reuse and disclosure

The test document and bundled fixtures are openly licensed under [Creative Commons Attribution 4.0](LICENSE.md). You may share and adapt them, including commercially, with attribution and a note of changes. The Markdific desktop app is a separate commercial product; its source code is not included or licensed by this repository.

Markdific created the pack and may be one of the products tested. Use the same document and scoring rules for every product, and disclose product-specific expectations rather than silently treating them as universal Markdown requirements.

## About Markdific

Markdific is a [Markdown viewer and editor](https://markdific.com/) for Mac, Windows, and Linux. Open `.md` files as formatted documents, edit visually or alongside a live preview, and export finished documents to PDF, Word, or HTML.
