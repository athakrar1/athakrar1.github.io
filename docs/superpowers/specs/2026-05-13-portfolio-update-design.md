# Portfolio Update Design
_2026-05-13_

## Goal

Update athakrar1.github.io to reflect Anjali's current professional identity as a creative technologist and ML engineer. The site currently reads as an undergrad portfolio (bio says "4th year undergrad") and is missing ~3 years of experience. No structural redesign — this is a targeted content update with light restructuring.

## Scope

Two files change: `index.html` (bio rewrite) and `experience.html` (new timeline entries, updated dates, new volunteering entries). No new project tiles or sections in this pass.

---

## Section 1: index.html — Bio Rewrite

Replace the entire bio block (currently three `<p>` tags including "4th year undergrad...", the interests paragraph, and the "Currently exploring/reading" lines) with:

**Paragraph 1 — Identity:**
> Hey, I'm Anjali! I'm a creative technologist and machine learning engineer at Meta Reality Labs, where I work on Codec Avatars — 3D body tracking, neural rendering, and the data pipelines that power them. I hold an M.S. and B.S. in EECS from UC Berkeley, with a concentration in computer vision.

**Paragraph 2 — Interests:**
> I'm drawn to work that sits at the intersection of the physical and the digital. My interests span **3D reconstruction, computational color, and computer graphics**, and I'm especially excited about the ways sensing and rendering technology can enable new kinds of experiences.

**Paragraph 3 — Currently (replaces "Currently exploring" and "Currently reading"):**
> *Currently:* collaborating with the Exploratorium's New Media Group on After Dark & exhibit development, and learning projection mapping.

The "For more info..." and "Feel free to check out..." lines are kept as-is.

---

## Section 2: experience.html — Timeline Updates

### Industry — two new entries at the top

**Meta Reality Labs • Codec Avatars** — June 2024–Present
_Machine Learning Engineer_
- Led development of evaluation pipelines for 3D body pose tracking & dense keypoint models: metrics, curation, analysis, optimization for large-scale runs
- Contributing researcher on CVPR 2026 paper, focusing on pretraining data generation & curation
- Designing VLM-powered tools for asset quality evaluation, large-scale dataset annotation, data exploration, and semantic retrieval across image and 3D asset-based datasets
- Prototyping physics-grounded neural networks to reduce implausible tracking errors in body pose estimation
- Implemented large-scale data compression, leading to a 128x reduction in storage needs

**Walt Disney Imagineering • Research and Development** — June–Aug 2023
_R&D Software Engineering Intern_
- Patent pending: Real-time 2D character segmentation, rigging, and face tracking pipeline for interactive experiences, achieving 50fps on Raspberry Pi (PyTorch, OpenCV, TouchDesigner)
- Fabricated a custom, LCD-based optical system to prototype animatronic eyes (Raspberry Pi, Fusion 360)

### Research — replace existing Ren Ng entry

Replace the "UC Berkeley Center for Innovation in Vision & Optics" entry (Jan 2023–Present, Oz Vision) with:

**Berkeley Artificial Intelligence Research (BAIR)** — Sept 2023–May 2024
_Graduate Researcher, advised by Prof. Ren Ng_
- Developed a novel image color correction technique to improve perceptual accuracy of photographed scenes; method combined multi-camera captures with spectral color theory (thesis: 3D Multispectral Colorimetry)
- Extended Gaussian Splatting to reconstruct multispectral 3D scenes from RAW multi-camera inputs, enabling pixel-aligned color mapping across arbitrary viewpoints

### Leadership — update end date

CS184 Head Student Instructor: change date from "Jan 2022 - Present" to "Jan 2022 - May 2024"

### Volunteering — two new entries

**Flaming Lotus Girls** — June–Aug 2025
- Contributed to fabrication and construction of the birds placed atop the large-scale kinetic sculpture

**Exploratorium, New Media Group** — March 2026–Present
- Collaborating with the New Media Group on After Dark programming and exhibit development

---

## Out of Scope (deferred)

- New project tiles for thesis (3D Multispectral Colorimetry) or Disney Imagineering work
- "from X to Y" contrast line in bio (placeholder for future iteration)
- Visual redesign or theme changes
