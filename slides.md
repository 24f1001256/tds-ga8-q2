---
marp: true
theme: default
paginate: true
size: 16:9
incremental: true
backgroundColor: "#ffffff"
style: |
  /* === Custom theme overrides === */
  section {
    font-family: Inter, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    color: #222;
  }

  h1 {
    color: #0b74de;
    letter-spacing: -0.5px;
  }

  .fixed-footer {
    position: fixed;
    right: 20px;
    bottom: 12px;
    font-size: 0.85rem;
    opacity: 0.85;
  }

  .meta {
    font-size: 0.9rem;
    opacity: 0.9;
  }

  .bg-overlay {
    background-color: rgba(0,0,0,0.35);
    color: #fff;
    padding: 1rem 1.2rem;
    border-radius: 8px;
    display: inline-block;
  }

  .card {
    padding: 1.2rem;
    border-radius: 8px;
    background: #ffffffdd;
    box-shadow: 0 6px 18px rgba(11,18,35,0.08);
  }
---

<div class="fixed-footer">
  <span class="meta">Doc owner: <strong>24f1001256@ds.study.iitm.ac.in</strong></span>
</div>

# Product Documentation — Core SDK  
**Version-controlled technical documentation with Marp**

---

## Why Marp + Git?

- Diffable markdown — easy PR reviews  
- Consistent slide output (HTML/PDF)  
- Works with CI workflows  
- Single-source documentation  

---

<!-- _background: "https://images.unsplash.com/photo-1508780709619-79562169bc64?w=1600&q=80" -->
# Visual Overview

<div class="bg-overlay">
  High-level architecture diagram and major components.
</div>

---

## Installation

```bash
npm install @our-company/sdk --save
