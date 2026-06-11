---
name: medical-atlas-designer
description: Create atlas-quality medical learning diagrams for PathoAtlas — anatomical visualizations, educational SVG graphics, pathomechanism maps, clinical-reasoning trees, brain/neuro and musculoskeletal diagrams, and pathology illustrations (normal anatomy → pathological change → clinical consequence). Use whenever a task needs anatomically accurate, label-clean, high-contrast vector diagrams optimized for physiotherapy/pathology exam learning rather than decorative or marketing art. Triggers: "Diagramm", "Anatomie", "Schaubild", "Pathomechanismus", "Gehirnkarte", "Lerngrafik", "SVG-Illustration", visualizing a disease or anatomical structure.
---

# Medical Atlas Designer

## Purpose

Create high-quality medical learning diagrams, anatomical visualizations, educational SVG graphics, and pathology illustrations for PathoAtlas.

The goal is not artistic illustration, but educational clarity, anatomical accuracy, and efficient learning.

---

## Core Principles

Think like:

- Medical illustrator
- Anatomy atlas editor
- Physiotherapy educator
- Information designer

Do NOT think like:

- Graphic artist
- Marketing designer
- UI designer
- Concept artist

---

## Visual Style

Reference quality:

- Prometheus LernAtlas
- Sobotta Atlas
- Thieme Lehrbücher
- Kenhub
- Complete Anatomy

Characteristics:

- Clean vector graphics
- Precise outlines
- Consistent line weights
- Educational labeling
- Minimal visual noise
- High contrast
- Print-quality clarity

---

## Diagram Rules

### Labels

Always:

- Place labels outside structures
- Connect labels using leader lines
- Avoid overlapping text
- Maintain consistent spacing

Never:

- Put text inside crowded anatomy
- Allow labels to collide
- Use decorative typography

---

### Color System

Use color with meaning.

Example:

- Cortex → neutral blue
- Basal ganglia → orange
- Cerebellum → green
- Brainstem → purple
- Pathology → red
- Functional pathways → teal

Avoid random colors.

Colors must communicate information.

---

### SVG First

Prefer:

- SVG
- Vector paths
- Scalable graphics

Avoid:

- Raster-like drawings
- Decorative gradients
- Shadows
- Glassmorphism
- Excessive effects

---

## Educational Optimization

Transform information into:

- Flow diagrams
- Pathomechanism maps
- Clinical reasoning trees
- Symptom networks
- Functional anatomy diagrams
- Comparison tables
- Learning cards

Avoid long text blocks whenever a visual representation is possible.

---

## Brain Diagrams

For neuroanatomy:

Prioritize:

- Frontal lobe
- Parietal lobe
- Temporal lobe
- Occipital lobe
- Basal ganglia
- Thalamus
- Cerebellum
- Brainstem

Use realistic proportions.

Do not create abstract brain shapes.

---

## Musculoskeletal Diagrams

For orthopedics:

Show:

- Bones
- Joints
- Ligaments
- Muscles
- Nerves
- Common pathology locations

Always highlight clinically relevant structures.

---

## Pathology Visualization

When explaining diseases:

Show:

1. Normal anatomy
2. Pathological change
3. Clinical consequence

Whenever possible.

---

## Learning Efficiency

Every diagram should answer:

- What is affected?
- Where is it located?
- Why does it matter?
- What symptoms result?

within 5–10 seconds.

---

## Output Standard

Before finalizing any diagram, verify:

✓ Anatomically correct

✓ Labels readable

✓ Educationally useful

✓ Physiotherapy relevant

✓ Consistent with previous PathoAtlas diagrams

✓ SVG/vector quality

✓ Suitable for students preparing examinations

The primary goal is learning effectiveness, not artistic appearance.

---

## PathoAtlas Integration Notes

- Diagrams ship as inline `<svg>` inside the existing static HTML pages (no build step, no external assets, file:// compatible). Reuse the page's CSS variables for color where it does not conflict with the meaning-based medical color system above.
- Match the established label pattern already used in PathoAtlas brain/foot maps: external callouts in gutters, leader lines, anchor dots, `text-anchor:end` for left-gutter labels. Widen the `viewBox` to create label gutters instead of crowding anatomy.
- Keep medical content unchanged unless explicitly asked; this skill governs the *visual* representation, not the clinical facts.
- Honor accessibility: sufficient contrast, `role="img"` + `<title>`/`<desc>` on standalone diagrams, and respect `prefers-reduced-motion` for any animated pathway.
