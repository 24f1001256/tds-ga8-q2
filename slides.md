---
marp: true
theme: default
paginate: true        # adds page number in footer
size: 16:9
incremental: true     # enables fragments (incremental reveal of lists)
backgroundColor: '#ffffff'
style: |
  /* === Custom theme overrides === */
  section {
    font-family: Inter, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    color: #222;
  }

  /* simple header accent */
  h1 {
    color: #0b74de;
    letter-spacing: -0.5px;
  }

  /* fixed footer shown on every slide */
  .fixed-footer {
    position: fixed;
    right: 20px;
    bottom: 12px;
    font-size: 0.85rem;
    opacity: 0.85;
  }

  /* small brand & metadata area */
  .meta { font-size: 0.9rem; opacity: .9; }

  /* code block sizing */
  pre code { font-size: 0.82rem; }

  /* background overlay for readability on image slide */
  .bg-overlay {
    background-color: rgba(0,0,0,0.36);
    color: #fff;
    padding: 1.25rem;
    border-radius: 8px;
    display: inline-block;
  }

  /* a simple card for content */
  .card {
    padding: 1.2rem;
    border-radius: 8px;
    box-shadow: 0 6px 18px rgba(11, 18, 35, 0.06);
    background: linear-gradient(180deg, #ffffff, #fbfcfe);
  }
---

<!-- Fixed footer (placed once; CSS makes it appear on every slide) -->
<div class="fixed-footer">
  <span class="meta">Doc owner: <strong>24f1001256@ds.study.iitm.ac.in</strong></span>
</div>

<!-- Slide 1: Title -->
# Product Documentation — Core SDK
**Maintainable, VCS-friendly docs for developers**

- Versioned Markdown (Marp) — single source, exportable to PDF/HTML/Slides
- Theme and CSS embedded for consistent exports

---

<!-- Slide 2: Why Marp + Git -->
## Why keep docs in Marp (Markdown) + Git?

1. Single-file, human-readable source (Markdown).  
2. Easily reviewed in PRs and diffable history.  
3. Export to multiple formats (PDF, HTML slides, PNG).  
4. Apply CI to auto-build artifacts.

---

<!-- background: url('https://images.unsplash.com/photo-1508780709619-79562169bc64?w=1600&q=80') center / cover -->
<!-- Slide 3: Background image slide -->
# Visual overview
<div class="bg-overlay">
  High-level architecture diagram and major components.
</div>

---

## Installation (Code sample)

```bash
# install via npm
npm install @our-company/sdk --save
