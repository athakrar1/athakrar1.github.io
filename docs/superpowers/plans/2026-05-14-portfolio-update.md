# Portfolio Update Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Update athakrar1.github.io to reflect Anjali's current professional identity as a creative technologist and ML engineer at Meta Reality Labs.

**Architecture:** Pure HTML content edits across two files. No build step, no dependencies, no tests — verification is visual (open in browser). Commits are frequent and scoped.

**Tech Stack:** HTML, plain CSS (existing Phantom theme)

---

## Files

- Modify: `index.html` — bio rewrite (lines 56–76)
- Modify: `experience.html` — industry entries, research entry, leadership date, volunteering entries

---

### Task 1: Rewrite bio in index.html

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Replace the bio block**

Find this block in `index.html` (starts at the `<header>` tag inside `<div class="inner">`):

```html
<header>
    <h1>Hey, I'm Anjali!<br /> </h1>
    <p> I'm a 4th year undergrad at UC Berkeley studying Electrical Engineering and Computer Science. 
        While at Cal, I've been head student instructor for <a href="https://cs184.eecs.berkeley.edu/sp23">Cal's computer graphics course (CS184)</a>, 
        <a href="https://intelligentimaging.ucsf.edu/">immersed myself in computer vision research</a>, and led a <a href="https://mdb.dev/">mobile development org</a></p>
        <!-- led a mobile development org</a>! -->

    <p> I'm passionate about <u>computer graphics, education, and tech for social good</u>. 
        I'm excited about the applications of machine learning to these spaces, 
        and am specifically interested in  <u>simulation tech, 3D computer vision, and computational photography</u>. 
        After graduating, I hope to operate at the intersection of product and research, applying the latest and greatest 
        technology to real-world, high-impact problems. </p>									
        
    </a></p>
    
    
    <p> <i>Currently exploring:</i>  <a href="http://roorda.vision.berkeley.edu/">human vision</a> (Research with Prof. Ren Ng & Prof. Austin Roorda), <a href="http://www.ucbugg.com/static/index.html">making animated shorts</a> (Maya), hiking trails in the Berkeley hills!</p>
    <p> <i>Currently reading:</i> <i>The Design of Everyday Things</i> by Don Norman, <i>On Photography</i> by Susan Sontag </p>

    <p> <b>For more info about my experience, click <a href="experience.html">here!</a> </b></p>

    <p> Feel free to check out a few of my projects below :)</p>
</header>
```

Replace with:

```html
<header>
    <h1>Hey, I'm Anjali!<br /> </h1>
    <p>I'm a creative technologist and machine learning engineer at Meta Reality Labs, where I work on Codec Avatars — 3D body tracking, neural rendering, and the data pipelines that power them. I hold an M.S. and B.S. in EECS from UC Berkeley, with a concentration in computer vision.</p>

    <p>I'm drawn to work that sits at the intersection of the physical and the digital. My interests span <b>3D reconstruction, computational color, and computer graphics</b>, and I'm especially excited about the ways sensing and rendering technology can enable new kinds of experiences. I have previously worked at Disney Imagineering R&D, UCSB Media Arts and Tech Lab, and the UCSF Big Data in Radiology Lab.</p>

    <p><i>Currently:</i> collaborating with the Exploratorium's New Media Group on After Dark &amp; exhibit development, and learning projection mapping.</p>

    <p> <b>For more info about my experience, click <a href="experience.html">here!</a> </b></p>

    <p> Feel free to check out a few of my projects below :)</p>
</header>
```

- [ ] **Step 2: Verify in browser**

Open `index.html` in a browser. Confirm:
- Bio reads "creative technologist and machine learning engineer at Meta Reality Labs"
- No mention of "4th year undergrad"
- "Currently" line mentions Exploratorium and projection mapping
- "Currently reading" line is gone

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "update bio to reflect current professional identity"
```

---

### Task 2: Add Codec Avatars and Disney Imagineering to Industry timeline

**Files:**
- Modify: `experience.html`

- [ ] **Step 1: Add two new entries at the top of the Industry `<ul class="timeline">`**

Find the opening of the Industry timeline in `experience.html`:

```html
<ul class="timeline">
    <li> <a target="_blank" href="https://about.meta.com/realitylabs/">Meta Reality Labs</a> <p style="float: right">May - Aug 2022</p>
```

Insert the following two `<li>` entries immediately before that existing `<li>`:

```html
<li> <a target="_blank" href="https://about.meta.com/realitylabs/">Meta Reality Labs • Codec Avatars</a> <p style="float: right">June 2024 - Present</p>
    <i><p style="margin:0">Machine Learning Engineer</p></i>
    <ul>
        <li>Computer vision R&amp;D for photorealistic avatars (Codec Avatars)</li>
    </ul>
</li>
<li> <a target="_blank" href="https://www.disneyimagineering.com/">Walt Disney Imagineering • Research and Development</a> <p style="float: right">June - Aug 2023</p>
    <i><p style="margin:0">R&amp;D Software Engineering Intern</p></i>
    <ul>
        <li>Interactive exhibit development: mocap/body tracking, fabrication, experience design!</li>
    </ul>
</li>
```

- [ ] **Step 2: Verify in browser**

Open `experience.html`. Confirm:
- "Meta Reality Labs • Codec Avatars" appears at the top of the Industry section, dated June 2024–Present
- "Walt Disney Imagineering • Research and Development" appears second, dated June–Aug 2023
- Existing entries (Meta XR Holograms 2022, Facebook Reality Labs 2021, Oracle 2020) are still present below

- [ ] **Step 3: Commit**

```bash
git add experience.html
git commit -m "add Codec Avatars and Disney Imagineering to industry timeline"
```

---

### Task 3: Replace BAIR research entry

**Files:**
- Modify: `experience.html`

- [ ] **Step 1: Replace the UC Berkeley Center for Innovation in Vision & Optics entry**

Find this block in the Research `<ul class="timeline">`:

```html
<li> <a target="_blank" href="http://roorda.vision.berkeley.edu/">UC Berkeley Center for Innovation in Vision & Optics</a> <p style="float: right">Jan 2023 - Present</p> 
    <i><p style="margin:0"> Undergraduate Researcher</p></i>
    <ul>
        <li>
            Developing experiments for Oz Vision
        </li>
        <li>
            PIs: Prof. Ren Ng, Prof. Austin Roorda 
        </li>
    </ul>
</li>
```

Replace with:

```html
<li> <a target="_blank" href="https://bair.berkeley.edu/">Berkeley Artificial Intelligence Research (BAIR)</a> <p style="float: right">Sept 2023 - May 2024</p>
    <i><p style="margin:0">Graduate Researcher, advised by Prof. Ren Ng</p></i>
    <ul>
        <li>Developed a novel image color correction technique to improve perceptual accuracy of photographed scenes (thesis: 3D Multispectral Colorimetry)</li>
    </ul>
</li>
```

- [ ] **Step 2: Verify in browser**

Open `experience.html`. In the Research section confirm:
- "Berkeley Artificial Intelligence Research (BAIR)" appears, dated Sept 2023–May 2024
- "UC Berkeley Center for Innovation in Vision & Optics" / Oz Vision entry is gone
- UCSF, Sequin Lab, and UCSB entries are still present

- [ ] **Step 3: Commit**

```bash
git add experience.html
git commit -m "replace Oz Vision entry with BAIR graduate research"
```

---

### Task 4: Update CS184 end date

**Files:**
- Modify: `experience.html`

- [ ] **Step 1: Update the date**

Find this line in the Leadership section:

```html
<li> <a target="_blank" href="">CS184: Computer Graphics & Imaging </a> <p style="float: right">Jan 2022 - Present</p>
```

Change to:

```html
<li> <a target="_blank" href="">CS184: Computer Graphics & Imaging </a> <p style="float: right">Jan 2022 - May 2024</p>
```

- [ ] **Step 2: Verify in browser**

Open `experience.html`. In the Leadership section confirm CS184 shows "Jan 2022 - May 2024".

- [ ] **Step 3: Commit**

```bash
git add experience.html
git commit -m "update CS184 end date to May 2024"
```

---

### Task 5: Add Exploratorium and Flaming Lotus Girls to Volunteering

**Files:**
- Modify: `experience.html`

- [ ] **Step 1: Add two new entries at the top of the Volunteering `<ul class="timeline">`**

Find the opening of the Volunteering & Campus Involvement timeline:

```html
<li> <a target="_blank" href="https://advocate.berkeley.edu/">Student Advocate's Office</a> <p style="float: right">Aug 2021 - Dec 2022</p>
```

Insert the following two `<li>` entries immediately before it:

```html
<li> <a target="_blank" href="https://www.exploratorium.edu/">Exploratorium, New Media Group</a> <p style="float: right">March 2026 - Present</p>
    <ul>
        <li>Collaborating with the New Media Group on After Dark programming and exhibit development</li>
    </ul>
</li>
<li> <a target="_blank" href="https://flaminglotus.com/">Flaming Lotus Girls</a> <p style="float: right">June - Aug 2025</p>
    <ul>
        <li>Contributed to fabrication and construction of the birds placed atop the large-scale kinetic sculpture</li>
    </ul>
</li>
```

- [ ] **Step 2: Verify in browser**

Open `experience.html`. In the Volunteering section confirm:
- "Exploratorium, New Media Group" appears at the top, dated March 2026–Present
- "Flaming Lotus Girls" appears second, dated June–Aug 2025
- Student Advocate's Office, Uncuffed, and other existing entries are still present

- [ ] **Step 3: Commit**

```bash
git add experience.html
git commit -m "add Exploratorium and Flaming Lotus Girls to volunteering"
```
