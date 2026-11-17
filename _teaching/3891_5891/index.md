---
layout: page
title: CC 3891 / 5891 Foundations of Computational Biology
term: Spring 2027
semester: Spring 2027
type: Undergraduate / Graduate
category: Undergraduate
importance: 2        # lower = shows earlier
nav: true
permalink: /courses/3891_5891/
---

<style>
  .fcb { --teal:#0f766e; --violet:#7c3aed; --amber:#b45309; --blue:#1d4ed8; line-height:1.65; }
  .fcb h2 { margin-top:2.5rem; font-weight:700; }
  .fcb .lead { font-size:1.25rem; color:#444; margin:.25rem 0 1rem; }
  .fcb .hero img { width:100%; height:auto; border-radius:16px; border:1px solid #e9dccb; }
  .fcb .badges { display:flex; flex-wrap:wrap; gap:.5rem; margin:1rem 0 0; }
  .fcb .badge-pill { padding:.3rem .8rem; border-radius:999px; background:#fff; border:1px solid #e9dccb; font-weight:600; font-size:.9rem; }
  .fcb .questions { display:grid; grid-template-columns:repeat(auto-fit,minmax(240px,1fr)); gap:1rem; margin:1rem 0; }
  .fcb .q { padding:1.1rem 1.25rem; border-left:5px solid var(--teal); background:#fff; border-radius:8px; box-shadow:0 1px 3px rgba(0,0,0,.08); font-size:1.05rem; font-weight:600; }
  .fcb .q:nth-child(2) { border-color:var(--violet); }
  .fcb .q:nth-child(3) { border-color:var(--blue); }
  .fcb .themes { display:grid; grid-template-columns:repeat(auto-fit,minmax(260px,1fr)); gap:1.25rem; margin:1rem 0; }
  .fcb .theme { background:#fff; border-radius:14px; border:1px solid #e9dccb; border-top:6px solid var(--c); overflow:hidden; box-shadow:0 2px 6px rgba(0,0,0,.07); }
  .fcb .theme img { display:block; width:100%; height:110px; object-fit:contain; background:var(--bg); padding:.5rem; }
  .fcb .theme .body { padding:1rem 1.25rem 1.25rem; }
  .fcb .theme h3 { margin:0 0 .25rem; font-size:1.2rem; color:var(--c); }
  .fcb .theme .bq { font-style:italic; margin:0 0 .75rem; color:#333; }
  .fcb .theme dl { margin:0; font-size:.95rem; }
  .fcb .theme dt { font-size:.75rem; letter-spacing:.06em; text-transform:uppercase; color:#666; margin-top:.5rem; }
  .fcb .theme dd { margin:0; }
  .fcb .t1 { --c:var(--teal); --bg:#f0fdfa; }
  .fcb .t2 { --c:var(--violet); --bg:#f5f3ff; }
  .fcb .t3 { --c:var(--amber); --bg:#fffbeb; }
  .fcb .t4 { --c:var(--blue); --bg:#eff6ff; }
  .fcb .reg { display:grid; grid-template-columns:repeat(auto-fit,minmax(240px,1fr)); gap:1rem; margin:1rem 0; }
  .fcb .reg-card { text-align:center; padding:1.5rem 1rem; border-radius:14px; background:#fff; border:2px solid var(--teal); }
  .fcb .reg-card.g { border-color:var(--violet); }
  .fcb .reg-card .num { font-size:2rem; font-weight:800; }
  .fcb .reg-card .lvl { color:#555; }
  .fcb .placeholder { background:#fff3cd; border:1px dashed #b58900; border-radius:6px; padding:.1rem .45rem; font-size:.9em; }
</style>

<div class="fcb" markdown="1">

<div class="hero">
  <img src="{{ '/assets/img/cc3891/hero.svg' | relative_url }}" alt="Illustration: DNA, a cluster of cells, a tissue map and a network, connected by a dotted line">
</div>

<p class="lead">From DNA to cells to disease: understanding biology through computation.</p>

<div class="badges">
  <span class="badge-pill">CC 3891 · Undergraduate</span>
  <span class="badge-pill">CC 5891 · Graduate</span>
  <span class="badge-pill">Spring 2027</span>
  <span class="badge-pill">Instructor: Hirak Sarkar</span>
</div>

## Big questions in biology

<div class="questions">
  <div class="q">How does a single cell carry the instructions to build an entire organism?</div>
  <div class="q">How do billions of cells acquire different identities and work together?</div>
  <div class="q">Can we use computational models to understand and predict disease?</div>
</div>

Modern experiments turn these questions into data: the letters of a genome, the activity of thousands
of genes in each of millions of cells, the positions of those cells inside a tissue. Nobody can read
that by eye. Algorithms, mathematics and machine learning let us find the pattern, ask whether it is
real, and connect it back to the biology.

This course introduces those computational ideas and lets you use them on real biological datasets.

## Explore biology through code

Four themes, each starting from a biological question and building a computational idea to answer
it. You will work with a few widely used Python tools along the way; the tools are there to help you
explore the ideas, not as separate subjects to master.

<div class="themes">
  <div class="theme t1">
    <img src="{{ '/assets/img/cc3891/genomes.svg' | relative_url }}" alt="Two aligned DNA sequences with one mismatch">
    <div class="body">
      <h3>Explore genomes</h3>
      <p class="bq">How similar are two stretches of DNA, and how do we piece a genome together from short reads?</p>
      <dl>
        <dt>Concepts</dt><dd>DNA sequences, alignment, genome assembly, dynamic programming</dd>
        <dt>Tools</dt><dd>Biopython, BLAST, and a sampling of aligners and assemblers (e.g. minimap2, BWA, MAFFT, SPAdes)</dd>
      </dl>
    </div>
  </div>
  <div class="theme t2">
    <img src="{{ '/assets/img/cc3891/cells.svg' | relative_url }}" alt="Cells grouped into three clusters">
    <div class="body">
      <h3>Discover cell types</h3>
      <p class="bq">Which cells in a sample are alike, and how many kinds are there?</p>
      <dl>
        <dt>Concepts</dt><dd>Gene expression, PCA, clustering, UMAP</dd>
        <dt>Tools</dt><dd>Scanpy</dd>
      </dl>
    </div>
  </div>
  <div class="theme t3">
    <img src="{{ '/assets/img/cc3891/tissues.svg' | relative_url }}" alt="A tissue with cells connected to their neighbors">
    <div class="body">
      <h3>Map tissues</h3>
      <p class="bq">Does where a cell sits tell us something about what it does?</p>
      <dl>
        <dt>Concepts</dt><dd>Spatial organization, graphs, cellular neighborhoods</dd>
        <dt>Tools</dt><dd>Squidpy</dd>
      </dl>
    </div>
  </div>
  <div class="theme t4">
    <img src="{{ '/assets/img/cc3891/models.svg' | relative_url }}" alt="A small neural network">
    <div class="body">
      <h3>Build predictive models</h3>
      <p class="bq">Can a model learn to tell healthy from diseased from the data alone?</p>
      <dl>
        <dt>Concepts</dt><dd>Classification, representation learning</dd>
        <dt>Tools</dt><dd>scikit-learn, introductory PyTorch</dd>
      </dl>
    </div>
  </div>
</div>

## What you will learn

By the end of the course you should be able to:

- **Translate** a biological question into a computational problem.
- **Analyze and visualize** real biological datasets using Python.
- **Understand** foundational algorithms and machine-learning concepts.
- **Investigate** genes, cells and the organization of tissues.
- **Interpret** computational results in their biological context.

## Who should take this course?

Anyone curious about where computing meets biology, whether you come from computer science,
biology, biomedical engineering, mathematics or data science. Undergraduates (CC 3891) and graduate
students (CC 5891) are both welcome and learn together.

- **Prerequisites:** <span class="placeholder">TODO: to be confirmed</span>
- **Expectations for CC 3891 (undergraduate):** <span class="placeholder">TODO: to be confirmed</span>
- **Expectations for CC 5891 (graduate):** <span class="placeholder">TODO: to be confirmed</span>
- **Grading, schedule and assignments:** <span class="placeholder">TODO: to be announced</span>
- **Meeting time and location:** <span class="placeholder">TODO: to be announced</span>

## Registration

<div class="reg">
  <div class="reg-card">
    <div class="num">CC 3891</div>
    <div class="lvl">Undergraduate · Spring 2027</div>
  </div>
  <div class="reg-card g">
    <div class="num">CC 5891</div>
    <div class="lvl">Graduate · Spring 2027</div>
  </div>
</div>

Find the course by searching for **CC 3891** or **CC 5891** in the Spring 2027 term on
[Vanderbilt YES](https://yes.vanderbilt.edu). Section and class number: <span class="placeholder">TODO: add once listed</span>.
Questions? Contact the instructor, [Hirak Sarkar]({{ "/" | relative_url }}).

</div>
