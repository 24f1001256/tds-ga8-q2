---
marp: true
theme: custom
paginate: true
class: lead
---

<!--
  Marp presentation: Product documentation
  Author contact: 24f1001256@ds.study.iitm.ac.in
  Notes:
    - Custom CSS theme is embedded below.
    - Page numbers enabled via `paginate: true`.
-->

<style>
/* === Custom theme overrides for Marp ===
   This block defines a simple, maintainable theme.
   Adjust colors, fonts, spacing to match corporate brand.
*/
:root {
  --brand-primary: #0b5fff;
  --brand-accent: #00a676;
  --text-color: #1f2937;
  --muted: #6b7280;
  --bg: #ffffff;
  --code-bg: rgba(11, 95, 255, 0.06);
}

section {
  font-family: "Inter", "Helvetica Neue", Arial, sans-serif;
  color: var(--text-color);
  background: var(--bg);
  padding: 36px;
}

/* Title styling */
h1 {
  color: var(--brand-primary);
  font-size: 48px;
  margin-bottom: 4px;
}
h2 { color: var(--brand-primary); }

/* Email badge */
.email {
  display: inline-block;
  padding: 6px 10px;
  border-radius: 6px;
  background: rgba(11,95,255,0.08);
  color: var(--brand-primary);
  font-weight: 600;
  font-size: 0.95em;
}

/* Code block styling */
pre {
  background: var(--code-bg);
  border-radius: 8px;
  padding: 14px;
  overflow: auto;
}

/* Page number small tweak (Marp's paginate: true will add numbers; this adjusts appearance) */
@media print, screen {
  footer.marp-footer {
    color: var(--muted);
    font-size: 0.8em;
  }
}

/* Small note style for speaker guidance */
.speaker-note {
  font-size: 0.85em;
  color: var(--muted);
}

/* Fragment emphasis (works with Marp fragments) */
.reveal .fragment {
  transition: transform 300ms ease, opacity 300ms ease;
}
</style>

---

# Product Documentation — Release 1.4
**Marp** presentation for maintainable product docs  
Contact: <span class="email">24f1001256@ds.study.iitm.ac.in</span>

---

<!-- backgroundImage: url('assets/architecture-hero.jpg') -->
<!-- background-size: cover -->
<!-- background-position: center -->

# System Overview
This slide uses a **background image** (see directive above).  
Use `assets/architecture-hero.jpg` in the same repo `assets/` folder.

---

## Table of contents
1. Product overview
2. Architecture & diagrams
3. API examples
4. Performance & complexity
5. FAQs

---

## Product overview (Markdown slide)

- **Name:** Acme Core Engine  
- **Version:** 1.4.0 <span class="fragment">(LTS)</span>  
- **Primary goal:** Reliable, low-latency processing of transaction streams.  
- **Contact:** <span class="email">24f1001256@ds.study.iitm.ac.in</span>

> This slide is written in **Markdown** and supports Marp directives and fragments.

---

## Architecture — Key Components
- Ingest pipeline <span class="fragment">(Kafka)</span>
- Stream processor <span class="fragment">(Flink)</span>
- Storage <span class="fragment">(Postgres + S3)</span>

---

## Code sample — Example API usage

```javascript
// GET product details
fetch('/api/v1/products/42')
  .then(r => r.json())
  .then(data => console.log('Product', data));

Algorithmic complexity (math)

We use a deduplication algorithm with expected complexity:

Time complexity: 
  
𝑇
(
𝑛
)
=
𝑂
(
𝑛
log
⁡
𝑛
)
Time complexity: T(n)=O(nlogn)

For streaming deduplication using a hash + small-heap window:

Space complexity: 
  
𝑆
(
𝑛
)
=
𝑂
(
𝑘
)
(where 
𝑘
 is window size)
Space complexity: S(n)=O(k)(where k is window size)
Adjust max.inflight.requests to match I/O concurrency <span class="fragment">— prevents head-of-line blocking</span>

Slide with fragments (animated reveals)

First point <span class="fragment">— reveal 1</span>

Second point <span class="fragment">— reveal 2</span>

Final point <span class="fragment">— reveal 3</span>

Speaker notes

Notes are included under each slide body using the .speaker-note style.

Speaker guidance: walk through the architecture diagram, emphasize reliability SLAs and monitoring hooks.
Assets & structure (suggested)
/ (repo root)
├─ slides.md                # this file
├─ assets/
│  ├─ architecture-hero.jpg
│  └─ logo.png
└─ README.md

Exporting & CI

Use Marp CLI to convert to PDF/HTML:

npx @marp-team/marp-cli slides.md -o slides.pdf

npx @marp-team/marp-cli slides.md -o slides.html

Add a GitHub Actions workflow to run Marp on push and attach artifacts for releases.

Thank you

Questions? Reach me at <span class="email">24f1001256@ds.study.iitm.ac.in</span>

---

### Notes & tips
- Put the background image at `assets/architecture-hero.jpg` in the same repo so the relative link works.
- The top front-matter `paginate: true` enables page numbers when rendered by Marp.
- The `<style>` block defines a lightweight custom theme — you can put this CSS into a separate `.css` theme file and set `theme: /path/to/custom.css` if you prefer.
- To produce the raw GitHub URL use the pattern:
