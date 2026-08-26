---
layout: page
title: CS6362 Advanced Machine Learning
term: Fall 2026
semester: Fall 2026
type: Graduate
category: Graduate
importance: 0        # lower = shows earlier
nav: true
toc:
  sidebar: left
permalink: /courses/CS6362-F26/
---

## 🧭 Description

This is a course on machine learning that studies different types of **learning scenarios**. A
scenario is characterized by four choices:

1. **The specification of our model.** Is the model linear? A neural network? This course is not
   focused on the details of model design — we assume a model has parameters that can be learned,
   accepts something as input, and produces something as output.
2. **The input provided for learning.** How many data items? What dimensionality? How many
   labeled examples?
3. **The output of the model.** Are we making predictions about a given data item, or generating
   novel data? If predicting — regression or classification?
4. **What we expect from the learning method.** Are we seeking the *best* model, or a *set* of
   good models?

The course is about **algorithms for learning** across these axes. The first half covers
fundamentals of **optimization** and **inference**; the second half builds on those foundations
through the **foundation-model era** — generative modeling, self-supervised representations,
sequence models, scaling, post-training, interpretability, and evaluation.

<br><br>
<span style="color:#8e2de2;font-weight:600;">💡 The emphasis is on <i>why</i> these methods work — deriving them from first principles — so you can adapt and extend them, not only apply them.</span>

## 🧱 Module Structure

The course is divided into six modules. Readings for each lecture are listed in the
[schedule](#️-schedule).

| Module | Core question | Topics |
|---|---|---|
| **I. Fundamentals of optimization**<br><i>Weeks 1–3</i> | What solution does learning actually find? | Gradient descent and stochastic gradient descent; convergence; lazy training and the neural tangent kernel; interpolation, double descent, implicit bias |
| **II. Fundamentals of inference**<br><i>Weeks 3–6</i> | What do we believe about a model, and how uncertain are we? | Bayesian statistics; Gaussian processes; model selection; Laplace approximation and the ELBO; variational inference; Monte Carlo and MCMC; Bayesian neural networks; out-of-distribution detection |
| **III. Generative modeling**<br><i>Weeks 7–10</i> | How can we represent and fit complex distributions? | EM and latent-variable models; variational autoencoders; posterior collapse; discrete latents; adversarial objectives and their instability; normalizing flows; energy-based models; score matching; diffusion; flow matching |
| **IV. Self-supervised learning**<br><i>Weeks 10–11</i> | What can we learn without labels? | Contrastive and non-contrastive objectives; representation collapse; attention and the Transformer as self-supervised pretraining |
| **V. Scale and post-training**<br><i>Weeks 12–13</i> | What changes when scale and post-training dominate? | Scaling laws; compute-optimal training; systems constraints on model design; RLHF; direct preference optimization; reasoning models and verifiable rewards |
| **VI. Interpretability and evaluation**<br><i>Week 15</i> | How do we understand and evaluate what we have built? | Superposition; sparse autoencoders and feature recovery; tool use and long-horizon agents; benchmark design and validity |

Modules I and II treat the supervised setting: regression, Gaussian processes and Bayesian neural
networks all predict a label from an input. Module III turns to models that produce samples rather
than predictions, Module IV to learning without labels, Module V to training at scale, and Module VI
to inspecting and evaluating the resulting systems.

## Logistics

- **Course Code:** CS6362
- **Term:** Fall 2026
- **Class Times:** Mondays & Wednesdays <i>03:35 PM - 04:50 PM</i>
- **Location:** Featheringill Hall 129
- **Instructor:** Hirak Sarkar — <a href="mailto:{{ 'hirak.sarkar@vanderbilt.edu' | encode_email }}">hirak.sarkar@vanderbilt.edu</a>
- **Teaching Assistant:** Huy Tran — <a href="mailto:{{ 'huy.tran@vanderbilt.edu' | encode_email }}">huy.tran@vanderbilt.edu</a>
- **Office Hours:** TBD

## 🎯 Learning Goals

By the end of this course, students will be able to:

- **Analyze** gradient descent and its stochastic variants — why they work, and their limitations
- **Explain** what solution SGD converges to: interpolation, double descent, implicit bias
- **Formulate** learning problems as Bayesian inference and reason about closed-form posteriors
- **Derive** and **implement** approximate inference — Laplace, variational inference, MCMC
- **Build** and **critique** generative models: VAEs, GANs, flows, score matching, diffusion
- **Compare** self-supervised objectives and explain what representations they encode
- **Reason** about scale: scaling laws, compute-optimal training, and post-training methods
- **Interpret** and **evaluate** deployed models — features, agent behavior, and benchmark validity
- **Read** and **reconstruct** results from current machine learning research literature

## 🏗️ Syllabus

This course is **lecture-based**, delivered primarily through slides with occasional whiteboard
work. Slides will be posted to this page.

### Assignments

Programming assignments run throughout the semester, in **Python**. We use **NumPy** for matrix
computations — experience with multidimensional arrays, slicing, and broadcasting is expected — and
where relevant [**JAX**](https://github.com/google/jax) for automatic differentiation.

Assignments build on provided boilerplate code. Where that is the case, you **may not import
additional Python libraries** beyond those included with the assignment; doing so forfeits credit
for the assignment. Include instructions for running your code, and submit as an archive.

### Quizzes

Brief (15–20 minute) **pop quizzes** of 1–2 questions on the current or previous lectures,
distributed randomly across the semester and completed at the end of class. Closed book, closed
phone, closed *any* device — bring a pen or pencil.

**Missing class when a quiz occurs, or arriving more than 25 minutes late, means *zero credit* for
that quiz; exceptions are case-by-case (e.g. medical absence). Your lowest quiz score is
dropped.**

### Project

The latter half of the semester is devoted to a research project in teams of **1–2**. You will go
in depth on a topic covered in class, situated in recent research — papers from roughly the last
five years at ICML, NeurIPS, ICLR, and relevant venues in vision (CVPR, ICCV, ECCV) and NLP (ACL,
EMNLP, NAACL-HLT).

- **Proposal** (~3 pages): basic information, brief description, **hypotheses** (the most important
  part), a literature survey of 4–5 papers, data (*make sure it exists and is accessible*), an
  evaluation plan, and a project plan. Also presented to the class.
- **Midway report** (~5 pages): refined aims and hypotheses, a fuller survey of 10–15 papers,
  methods, experimental design, and any refinement of the plan.
- **Presentation** to the class at the end of the semester.
- **Final submission** (8 pages excluding references), in the form of a research paper —
  introduction, related work, methods, experiments, discussion — plus all code and documentation.

Written portions use the [NeurIPS](https://nips.cc/Conferences/2023/PaperInformation/StyleFiles)
LaTeX style, preprint mode. Standard ML libraries such as
[PyTorch](https://github.com/pytorch/pytorch) or [Flax](https://github.com/google/flax) are
permitted, but **projects that use publicly-available code for a paper are not allowed** — the
point is to gain experience implementing algorithms and evaluating them experimentally.

## 🗓️ Schedule

<style>
table.wide {
  width: 100%;
  font-size: 0.85em;
  border-collapse: collapse;
}
table.wide th, table.wide td {
  border: 1px solid #ddd;
  padding: 6px 10px;
  vertical-align: top;
}
table.wide th {
  background-color: #f5f5f5;
  text-align: left;
}

table.wide th:nth-child(1),
table.wide td:nth-child(1) { width: 16%; }
table.wide th:nth-child(3),
table.wide td:nth-child(3) { width: 34%; }

/* Purple pill buttons */
.pill {
  display: inline-block;
  padding: 8px 16px;
  background: #8e2de2;
  color: #fff;
  font-weight: 700;
  font-size: 14px;
  line-height: 1;
  border-radius: 9999px;
  text-decoration: none;
  box-shadow: 0 6px 14px rgba(142,45,226,0.35);
  letter-spacing: 0.2px;
  transition: transform .12s ease, box-shadow .12s ease, opacity .12s ease;
}
.pill:hover {
  transform: translateY(-1px);
  box-shadow: 0 10px 24px rgba(142,45,226,0.35);
}
.pill:active { transform: translateY(0); }
.pill:focus { outline: 3px solid rgba(142,45,226,0.35); outline-offset: 2px; }

.pill--sm {
    padding: 2px 12px;
    font-size: 13px;
    background: rgba(142, 45, 226, 0.60);
    box-shadow: 0 3px 8px rgba(142, 45, 226, 0.20);
    backdrop-filter: blur(3px);
}

.paper-link {
  text-decoration: underline;
  color: #7b1fa2;
  font-weight: 600;
}
.due {
  font-weight: 600;
  color: #b3261e;
}
.wk {
  background: rgba(142, 45, 226, 0.07);
  font-weight: 600;
}
.mod {
  background: rgba(142, 45, 226, 0.22);
  font-size: 1.02em;
  border-top: 2px solid #8e2de2 !important;
}
.mod .q {
  font-weight: 400;
  font-style: italic;
  opacity: 0.85;
}
</style>

<table class="wide">
<thead style="background: color-mix(in srgb, Canvas 85%, CanvasText 15%); color: CanvasText;">
<tr>
<th>Date</th>
<th>Topic</th>
<th>Reading</th>
<th>Assignments</th>
</tr>
</thead>
<tbody>

<tr class="mod"><td colspan="4">
  <b>Module I — Fundamentals of optimization</b><br>
  <span class="q">What solution does learning actually find?</span>
  {% comment %} instructor planning note — stripped from the built page
  <span>Spine: Robbins &amp; Monro → Bottou, Curtis &amp; Nocedal → Zhang et al. → Soudry et al. / Belkin et al.</span>
  {% endcomment %}
</td></tr>

<tr class="wk"><td colspan="4"><b>Week 1</b> (Aug 26) — Course introduction, ML basics</td></tr>
<tr>
  <td>Wed, Aug 26</td>
  <td>Course introduction, review on regression</td>
  <td><a href="https://mml-book.github.io/" class="paper-link">MML</a> Ch. 6.1–6.4, Ch. 8.1–8.2, Ch. 9.1–9.2;
      <a href="https://cs.nyu.edu/~mohri/mlbook/" class="paper-link">FML</a> App. C</td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 2</b> (Aug 31) — Gradient descent</td></tr>
<tr>
  <td>Mon, Aug 31</td>
  <td>Gradient descent</td>
  <td><a href="https://mml-book.github.io/" class="paper-link">MML</a> Ch. 5, Ch. 7.1;
      <a href="https://cs.nyu.edu/~mohri/mlbook/" class="paper-link">FML</a> App. A, B</td>
  <td></td>
</tr>
<tr>
  <td>Wed, Sep 02</td>
  <td>Stochastic gradient descent</td>
  <td><a href="https://epubs.siam.org/doi/10.1137/16M1080173" class="paper-link">LSML</a> Sec. 2–7;
      <a href="https://arxiv.org/pdf/2301.11235" class="paper-link">HCT</a> Ch. 5</td>
  <td></td>
</tr>
<tr>
  <td>Thu, Sep 03</td>
  <td></td>
  <td></td>
  <td><span class="due">Assignment 1 posted</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 3</b> (Sep 7) — Generalization; inference begins</td></tr>
<tr>
  <td>Mon, Sep 07</td>
  <td>What does SGD actually find? Lazy training and the neural tangent kernel; interpolation, double descent, implicit bias <span style="opacity:0.7;font-size:0.92em;">(Labor Day — class meets)</span></td>
  <td><a href="https://mml-book.github.io/" class="paper-link">MML</a> Ch. 12.4;
      <a href="https://arxiv.org/abs/1806.07572" class="paper-link">Neural tangent kernel</a>;
      <a href="https://arxiv.org/abs/1611.03530" class="paper-link">Zhang et al., Rethinking generalization</a>;
      <a href="https://arxiv.org/abs/1812.11118" class="paper-link">Belkin et al., Double descent</a>;
      <a href="https://arxiv.org/abs/1710.10345" class="paper-link">Soudry et al., Implicit bias</a></td>
  <td></td>
</tr>

<tr class="mod"><td colspan="4">
  <b>Module II — Fundamentals of inference</b><br>
  <span class="q">What do we believe about a model, and how uncertain are we?</span>
  {% comment %} instructor planning note — stripped from the built page
  <span>Spine: Bayes → Gaussian processes → Laplace / ELBO → variational inference → MCMC</span>
  {% endcomment %}
</td></tr>
<tr>
  <td>Wed, Sep 09</td>
  <td>Bayesian statistics, linear regression; Gaussian processes</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 2.3, Ch. 3.2, Ch. 15.2.1–15.2.4;
      <a href="https://gaussianprocess.org/gpml/chapters/" class="paper-link">GP</a> Ch. 2;
      <a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 3.7–3.8</td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 4</b> (Sep 14) — Approximate inference</td></tr>
<tr>
  <td>Mon, Sep 14</td>
  <td>Model selection, Laplace approximation, information theory basics, ELBO</td>
  <td><a href="https://probml.github.io/pml-book/book1.html" class="paper-link">PML-1</a> Ch. 6.1–6.2;
      <a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 5.1, Ch. 7.4, Ch. 10.1</td>
  <td><span class="due">Assignment 2 posted</span></td>
</tr>
<tr>
  <td>Wed, Sep 16</td>
  <td>Variational inference and gradient-based estimators</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 6.3.5, Ch. 10.2;
      <a href="https://www.jmlr.org/papers/volume21/19-346/19-346.pdf" class="paper-link">MCGE</a></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 5</b> (Sep 21) — Monte Carlo and MCMC</td></tr>
<tr>
  <td>Mon, Sep 21</td>
  <td>Monte Carlo, Markov chains</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 11.1–11.4, Ch. 12.1–12.2</td>
  <td></td>
</tr>
<tr>
  <td>Wed, Sep 23</td>
  <td>MCMC: Metropolis–Hastings, Gibbs sampling, mixture models, HMC</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 12.1–12.3, 12.5, Ch. 17.1–17.4</td>
  <td></td>
</tr>
<tr>
  <td>Fri, Sep 25</td>
  <td></td>
  <td></td>
  <td><span class="due">Assignment 2 due</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 6</b> (Sep 28) — Uncertainty; project proposals</td></tr>
<tr>
  <td>Mon, Sep 28</td>
  <td>Bayesian neural networks; out-of-distribution detection</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 17.1–17.4, Ch. 19.1–19.7</td>
  <td></td>
</tr>
<tr>
  <td>Wed, Sep 30</td>
  <td>Project introductions</td>
  <td></td>
  <td><span class="due">Proposal presentations</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 7</b> (Oct 5) — Midterm; generative modeling begins</td></tr>
<tr>
  <td>Mon, Oct 05</td>
  <td><b>Midterm</b></td>
  <td></td>
  <td><span class="due">Will be graded</span></td>
</tr>

<tr class="mod"><td colspan="4">
  <b>Module III — Generative modeling</b><br>
  <span class="q">How can we represent and fit complex distributions?</span>
  {% comment %} instructor planning note — stripped from the built page
  <span>Spine: EM → VAE → GAN → WGAN → Score matching → DDPM</span>
  {% endcomment %}
</td></tr>
<tr>
  <td>Wed, Oct 07</td>
  <td>EM and latent-variable models</td>
  <td><a href="https://doi.org/10.1111/j.2517-6161.1977.tb01600.x" class="paper-link">Dempster, Laird &amp; Rubin, EM</a></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 8</b> (Oct 12) — Variational autoencoders</td></tr>
<tr>
  <td>Mon, Oct 12</td>
  <td>Variational autoencoders: the ELBO revisited, posterior collapse</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 21.1–21.2, 21.4;
      <a href="https://arxiv.org/abs/1312.6114" class="paper-link">Kingma &amp; Welling, VAE</a></td>
  <td><span class="due">Assignment 3 posted</span></td>
</tr>
<tr>
  <td>Wed, Oct 14</td>
  <td>Variational autoencoders: disentanglement, discrete latents</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 21.3, 21.5–21.6;
      <a href="https://arxiv.org/abs/1711.00937" class="paper-link">VQ-VAE</a></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 9</b> (Oct 19) — Implicit and invertible models</td></tr>
<tr>
  <td>Mon, Oct 19</td>
  <td>Implicit models: GANs → WGAN — divergences, instability, mode collapse</td>
  <td><a href="https://arxiv.org/abs/1406.2661" class="paper-link">Goodfellow et al., GAN</a>;
      <a href="https://arxiv.org/abs/1701.07875" class="paper-link">Arjovsky et al., WGAN</a></td>
  <td></td>
</tr>
<tr>
  <td>Wed, Oct 21</td>
  <td>Normalizing flows; energy-based models</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 23–24;
      <a href="https://arxiv.org/abs/1505.05770" class="paper-link">Rezende &amp; Mohamed, Normalizing flows</a></td>
  <td></td>
</tr>
<tr>
  <td>Thu–Fri, Oct 22–23</td>
  <td><b>Fall Break</b> <span style="opacity:0.7;font-size:0.92em;">(Thu–Fri)</span></td>
  <td></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 10</b> (Oct 26) — Diffusion; self-supervision begins</td></tr>
<tr>
  <td>Mon, Oct 26</td>
  <td>Score matching → denoising diffusion (DDPM) → flow matching</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 25;
      <a href="https://www.jmlr.org/papers/v6/hyvarinen05a.html" class="paper-link">Hyvärinen, Score matching</a>;
      <a href="https://arxiv.org/abs/1907.05600" class="paper-link">Song &amp; Ermon, NCSN</a>;
      <a href="https://arxiv.org/abs/2006.11239" class="paper-link">Ho et al., DDPM</a>;
      <a href="https://arxiv.org/abs/2210.02747" class="paper-link">Lipman et al., Flow matching</a></td>
  <td></td>
</tr>

<tr class="mod"><td colspan="4">
  <b>Module IV — Self-supervised learning</b><br>
  <span class="q">What can we learn without labels?</span>
  {% comment %} instructor planning note — stripped from the built page
  <span>Spine: Word2Vec / SimCLR → BYOL / VICReg → Transformer</span>
  {% endcomment %}
</td></tr>
<tr>
  <td>Wed, Oct 28</td>
  <td>Contrastive self-supervision: Word2Vec → SimCLR</td>
  <td><a href="https://arxiv.org/abs/1301.3781" class="paper-link">Mikolov et al., Word2Vec</a>;
      <a href="https://arxiv.org/abs/2002.05709" class="paper-link">Chen et al., SimCLR</a></td>
  <td></td>
</tr>
<tr>
  <td>Fri, Oct 30</td>
  <td></td>
  <td></td>
  <td><span class="due">Assignment 3 due</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 11</b> (Nov 2) — Non-contrastive learning; attention</td></tr>
<tr>
  <td>Mon, Nov 02</td>
  <td>Non-contrastive self-supervision: BYOL, VICReg — why representations do not collapse</td>
  <td><a href="https://arxiv.org/abs/2006.07733" class="paper-link">Grill et al., BYOL</a>;
      <a href="https://arxiv.org/abs/2105.04906" class="paper-link">Bardes et al., VICReg</a></td>
  <td></td>
</tr>
<tr>
  <td>Wed, Nov 04</td>
  <td>Sequence models and attention: the Transformer as self-supervised pretraining</td>
  <td><a href="https://arxiv.org/abs/1706.03762" class="paper-link">Vaswani et al., Attention is all you need</a></td>
  <td></td>
</tr>

<tr class="mod"><td colspan="4">
  <b>Module V — Scale and post-training</b><br>
  <span class="q">What changes when scale and post-training dominate?</span>
  {% comment %} instructor planning note — stripped from the built page
  <span>Spine: Scaling laws → Chinchilla → FlashAttention → InstructGPT → DPO → R1</span>
  {% endcomment %}
</td></tr>

<tr class="wk"><td colspan="4"><b>Week 12</b> (Nov 9) — The economics of scale</td></tr>
<tr>
  <td>Mon, Nov 09</td>
  <td>Scaling laws and compute-optimal training</td>
  <td><a href="https://arxiv.org/abs/2001.08361" class="paper-link">Kaplan et al., Scaling laws</a>;
      <a href="https://arxiv.org/abs/2203.15556" class="paper-link">Hoffmann et al., Chinchilla</a></td>
  <td></td>
</tr>
<tr>
  <td>Wed, Nov 11</td>
  <td>How systems constraints shape model design: FlashAttention</td>
  <td><a href="https://arxiv.org/abs/2205.14135" class="paper-link">Dao et al., FlashAttention</a></td>
  <td></td>
</tr>
<tr>
  <td>Fri, Nov 13</td>
  <td></td>
  <td></td>
  <td><span class="due">Project midway report due</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 13</b> (Nov 16) — Post-training</td></tr>
<tr>
  <td>Mon, Nov 16</td>
  <td>Post-training: RLHF → preference optimization</td>
  <td><a href="https://arxiv.org/abs/2203.02155" class="paper-link">Ouyang et al., InstructGPT</a>;
      <a href="https://arxiv.org/abs/2305.18290" class="paper-link">Rafailov et al., DPO</a></td>
  <td></td>
</tr>
<tr>
  <td>Wed, Nov 18</td>
  <td>Reasoning models and verifiable rewards</td>
  <td><a href="https://arxiv.org/abs/2501.12948" class="paper-link">DeepSeek-R1</a></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 14</b> (Nov 21–29) — Thanksgiving holidays</td></tr>
<tr>
  <td>Nov 21–29</td>
  <td><b>No class — Thanksgiving holidays</b></td>
  <td></td>
  <td></td>
</tr>

<tr class="mod"><td colspan="4">
  <b>Module VI — Interpretability and evaluation</b><br>
  <span class="q">How do we understand and evaluate what we have built?</span>
  {% comment %} instructor planning note — stripped from the built page
  <span>Spine: Superposition → Sparse autoencoders → ReAct → SWE-agent → HELM / τ-bench</span>
  {% endcomment %}
</td></tr>

<tr class="wk"><td colspan="4"><b>Week 15</b> (Nov 30) — Interpretability, agents, evaluation</td></tr>
<tr>
  <td>Mon, Nov 30</td>
  <td>Mechanistic interpretability: superposition and sparse autoencoders</td>
  <td><a href="https://transformer-circuits.pub/2022/toy_model/index.html" class="paper-link">Elhage et al., Toy models of superposition</a>;
      <a href="https://transformer-circuits.pub/2023/monosemantic-features/index.html" class="paper-link">Bricken et al., Towards monosemanticity</a>;
      <a href="https://transformer-circuits.pub/2024/scaling-monosemanticity/index.html" class="paper-link">Templeton et al., Scaling monosemanticity</a></td>
  <td></td>
</tr>
<tr>
  <td>Wed, Dec 02</td>
  <td>Agents and evaluation: tool use, benchmark design and validity</td>
  <td><a href="https://arxiv.org/abs/2210.03629" class="paper-link">Yao et al., ReAct</a>;
      <a href="https://arxiv.org/abs/2405.15793" class="paper-link">Yang et al., SWE-agent</a>;
      <a href="https://arxiv.org/abs/2211.09110" class="paper-link">Liang et al., HELM</a>;
      <a href="https://arxiv.org/abs/2406.12045" class="paper-link">Yao et al., τ-bench</a></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 16</b> (Dec 7) — Project presentations</td></tr>
<tr>
  <td>Mon, Dec 07</td>
  <td><b>Project presentations I</b></td>
  <td></td>
  <td><span class="due">Will be graded</span></td>
</tr>
<tr>
  <td>Wed, Dec 09</td>
  <td><b>Project presentations II</b></td>
  <td></td>
  <td><span class="due">Will be graded</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Examination and reading period</b> (Dec 11–19)</td></tr>
<tr>
  <td>Dec 11–19</td>
  <td></td>
  <td></td>
  <td><span class="due">Project final submission due — date TBD</span></td>
</tr>

</tbody>
</table>

---

<!-- ## 🧩 Topics Covered

### Module I — Fundamentals of optimization

*What solution does learning actually find?*

Finding the best model parameters in the supervised setting. Gradient descent and stochastic
gradient descent: what they are, why they converge, and where they fail, with the necessary linear
algebra, probability and convexity.

Generalization: why an overparameterized model that can fit random labels still generalizes. Lazy
training and the neural tangent kernel, interpolation, double descent, and the implicit bias of
gradient descent.

### Module II — Fundamentals of inference

*What do we believe about a model, and how uncertain are we?*

Finding a set of models rather than one. Bayesian inference and the posterior over model
parameters, beginning with cases that admit a closed form: Bayesian statistics, parametric models,
Gaussian processes, and model selection. Where the posterior is intractable: Laplace approximation,
variational inference, Markov chain Monte Carlo, and neural network posteriors. Applications to
uncertainty estimation and out-of-distribution detection.

### Module III — Generative modeling

*How can we represent and fit complex distributions?*

Methods for fitting a distribution whose likelihood cannot be maximized directly. Latent-variable
models and EM optimize a bound. Variational autoencoders extend that bound with amortized inference:
the ELBO, posterior collapse, discrete latents. Implicit models replace the likelihood with a
two-sample objective: GANs and WGAN, divergences, instability, mode collapse. Normalizing flows
constrain the architecture so the likelihood stays exact. Energy-based models, score matching,
denoising diffusion and flow matching avoid normalization altogether.

### Module IV — Self-supervised learning

*What can we learn without labels?*

Supervision derived from the data itself: part of the input is hidden and predicted from the rest,
and the resulting representation is retained. Contrastive objectives (Word2Vec, SimCLR) and
non-contrastive objectives (BYOL, VICReg), and the conditions under which representations collapse.
The Transformer, whose next-token objective underlies the pretraining of modern language models.

### Module V — Scale and post-training

*What changes when scale and post-training dominate?*

Scaling laws and compute-optimal training, and the systems constraints that shape model design
(FlashAttention). Post-training: RLHF, direct preference optimization, which attains the same
objective without a reinforcement-learning loop, and reasoning models trained against verifiable
rewards.

### Module VI — Interpretability and evaluation

*How do we understand and evaluate what we have built?*

Mechanistic interpretability: superposition, and sparse autoencoders for recovering interpretable
features. Agents that use tools and act over long horizons. Evaluation: what benchmarks such as HELM
and τ-bench measure, and the ways benchmark design fails. -->

## 👥 Course Assessment (Tentative)

| Component | Weight |
|-----------|--------|
| **Assignments** | 45% |
| **Mid-term** | 10% |
| **Quizzes** | 10% |
| **Project** | 30% |
| - Proposal | 10% |
| - Midway Report | 5% |
| - Presentation | 5% |
| - Full Submission | 10% |
| **Class Participation** | 5% |

<!-- ### Grade scale

97+ : A+ &nbsp;·&nbsp; 94–97 : A &nbsp;·&nbsp; 90–94 : A− &nbsp;·&nbsp; 87–90 : B+ &nbsp;·&nbsp;
84–87 : B &nbsp;·&nbsp; 80–84 : B− &nbsp;·&nbsp; 77–80 : C+ &nbsp;·&nbsp; 74–77 : C &nbsp;·&nbsp;
70–74 : C− &nbsp;·&nbsp; 67–70 : D+ &nbsp;·&nbsp; 64–67 : D &nbsp;·&nbsp; 60–64 : D− &nbsp;·&nbsp;
&lt; 60 : F -->

### Late submission policy

One day late: 10% off &nbsp;·&nbsp; two days late: 20% off &nbsp;·&nbsp; past two days: no credit.
The exception is class presentations — no credit is given if you do not present in your allotted
time.

## 📋 Prerequisites

An introductory course in machine learning, plus sufficient background in **linear algebra** and
**probability and statistics**. Relevant mathematical background will be covered over the semester,
but what is covered in class should be treated as necessary rather than always sufficient — filling
remaining gaps is your responsibility.

## 📚 Textbooks and Reference Material

The schedule draws on the following books and review articles, referenced by abbreviation.

**Optimization**

- [**MML**](https://mml-book.github.io/) — Deisenroth, Faisal & Ong, *Mathematics for Machine Learning*
- [**FML**](https://cs.nyu.edu/~mohri/mlbook/) — Mohri, Rostamizadeh & Talwalkar, *Foundations of Machine Learning*
- [**LSML**](https://epubs.siam.org/doi/10.1137/16M1080173) — **Bottou et al.**, *Optimization Methods for Large-Scale Machine Learning* ([free arXiv version](https://arxiv.org/pdf/1606.04838))
- [**HCT**](https://arxiv.org/pdf/2301.11235) — **Garrigos et al.**, *Handbook of Convergence Theorems for (Stochastic) Gradient Methods*. Ch. 5 (Stochastic Gradient Descent) is assigned; Ch. 3 covers deterministic gradient descent

**Inference**

- [**PML-1**](https://probml.github.io/pml-book/book1.html) — Murphy, *Probabilistic Machine Learning: An Introduction*
- [**PML-2**](https://probml.github.io/pml-book/book2.html) — Murphy, *Probabilistic Machine Learning: Advanced Topics*
- [**GP**](https://gaussianprocess.org/gpml/chapters/) — Rasmussen & Williams, *Gaussian Processes for Machine Learning*
- [**MCGE**](https://www.jmlr.org/papers/volume21/19-346/19-346.pdf) — Mohamed, Rosca, Figurnov & Mnih, *Monte Carlo Gradient Estimation in Machine Learning*

The readings listed in the schedule are intended to **complement** the lecture slides.

### Reading list by module

Papers grouped by module, in the order covered. Per-lecture assignments are in the
[schedule](#️-schedule).

**Module I — Fundamentals of optimization**

- [Robbins & Monro (1951)](https://doi.org/10.1214/aoms/1177729586), *A Stochastic Approximation Method* — the origin of SGD
- **Bottou et al.**, [*Optimization Methods for Large-Scale Machine Learning*](https://arxiv.org/pdf/1606.04838) (**LSML**)
- **Garrigos et al.**, [*Handbook of Convergence Theorems for (Stochastic) Gradient Methods*](https://arxiv.org/pdf/2301.11235) (**HCT**) — Ch. 5 only
- **Jacot et al.**, [*Neural Tangent Kernel*](https://arxiv.org/abs/1806.07572)
- **Tancik et al.**, [*Fourier Features*](https://arxiv.org/pdf/2006.10739)
- **Zhang et al.**, [*Understanding Deep Learning Requires Rethinking Generalization*](https://arxiv.org/abs/1611.03530)
- **Belkin et al.**, [*Reconciling Modern Machine Learning Practice and the Bias–Variance Trade-off*](https://arxiv.org/abs/1812.11118) — double descent
- **Soudry et al.**, [*The Implicit Bias of Gradient Descent on Separable Data*](https://arxiv.org/abs/1710.10345)

**Module II — Fundamentals of inference**

Textbook readings: [**PML-1**](https://probml.github.io/pml-book/book1.html) Ch. 6,
[**PML-2**](https://probml.github.io/pml-book/book2.html) Ch. 2–3, 5–7, 10–12, 15, 17, 19, and
[**GP**](https://gaussianprocess.org/gpml/chapters/) Ch. 2. One article:

- **Mohamed et al.**, [*Monte Carlo Gradient Estimation in Machine Learning*](https://www.jmlr.org/papers/volume21/19-346/19-346.pdf) (**MCGE**)

**Module III — Generative modeling**

- [Dempster et al. (1977)](https://doi.org/10.1111/j.2517-6161.1977.tb01600.x), *Maximum Likelihood from Incomplete Data via the EM Algorithm*
- **Kingma et al.**, [*Auto-Encoding Variational Bayes*](https://arxiv.org/abs/1312.6114) — the VAE
- **van den Oord et al.**, [*Neural Discrete Representation Learning*](https://arxiv.org/abs/1711.00937) — VQ-VAE
- **Goodfellow et al.**, [*Generative Adversarial Networks*](https://arxiv.org/abs/1406.2661)
- **Arjovsky et al.**, [*Wasserstein GAN*](https://arxiv.org/abs/1701.07875)
- **Rezende et al.**, [*Variational Inference with Normalizing Flows*](https://arxiv.org/abs/1505.05770)
- **Hyvärinen et al.**, [*Estimation of Non-Normalized Statistical Models by Score Matching*](https://www.jmlr.org/papers/v6/hyvarinen05a.html)
- **Song et al.**, [*Generative Modeling by Estimating Gradients of the Data Distribution*](https://arxiv.org/abs/1907.05600)
- **Ho et al.**, [*Denoising Diffusion Probabilistic Models*](https://arxiv.org/abs/2006.11239)
- **Lipman et al.**, [*Flow Matching for Generative Modeling*](https://arxiv.org/abs/2210.02747)

**Module IV — Self-supervised learning**

- **Mikolov et al.**, [*Efficient Estimation of Word Representations in Vector Space*](https://arxiv.org/abs/1301.3781) — Word2Vec
- **Chen et al.**, [*A Simple Framework for Contrastive Learning of Visual Representations*](https://arxiv.org/abs/2002.05709) — SimCLR
- **Grill et al.**, [*Bootstrap Your Own Latent*](https://arxiv.org/abs/2006.07733) — BYOL
- **Bardes et al.**, [*VICReg: Variance-Invariance-Covariance Regularization*](https://arxiv.org/abs/2105.04906)
- **Vaswani et al.**, [*Attention Is All You Need*](https://arxiv.org/abs/1706.03762)

**Module V — Scale and post-training**

- **Kaplan et al.**, [*Scaling Laws for Neural Language Models*](https://arxiv.org/abs/2001.08361)
- **Hoffmann et al.**, [*Training Compute-Optimal Large Language Models*](https://arxiv.org/abs/2203.15556) — Chinchilla
- **Dao et al.**, [*FlashAttention*](https://arxiv.org/abs/2205.14135)
- **Ouyang et al.**, [*Training Language Models to Follow Instructions with Human Feedback*](https://arxiv.org/abs/2203.02155) — InstructGPT
- **Rafailov et al.**, [*Direct Preference Optimization*](https://arxiv.org/abs/2305.18290)
- **DeepSeek-AI et al.**, [*DeepSeek-R1*](https://arxiv.org/abs/2501.12948)

**Module VI — Interpretability and evaluation**

- **Elhage et al.**, [*Toy Models of Superposition*](https://transformer-circuits.pub/2022/toy_model/index.html)
- **Bricken et al.**, [*Towards Monosemanticity*](https://transformer-circuits.pub/2023/monosemantic-features/index.html) — sparse autoencoders
- **Templeton et al.**, [*Scaling Monosemanticity*](https://transformer-circuits.pub/2024/scaling-monosemanticity/index.html)
- **Yao et al.**, [*ReAct: Synergizing Reasoning and Acting in Language Models*](https://arxiv.org/abs/2210.03629)
- **Yang et al.**, [*SWE-agent*](https://arxiv.org/abs/2405.15793)
- **Liang et al.**, [*Holistic Evaluation of Language Models*](https://arxiv.org/abs/2211.09110) — HELM
- **Yao et al.**, [*τ-bench*](https://arxiv.org/abs/2406.12045)

## ⚖️ Policies

### Academic honesty

Students should adhere to the [Vanderbilt Honor System](https://www.vanderbilt.edu/student_handbook/the-honor-system/).
Cheating and plagiarism will not be tolerated. Do not copy, in any way, another student's work on
assignments. See also [Vanderbilt's Academic Integrity](https://www.vanderbilt.edu/studentaccountability/academic-integrity)
policies.

### Use of LLMs for completing assignments

Using large language models to complete assignments is acceptable provided you:

1. **Acknowledge** which specific LLM was used.
2. **Distinguish** your own work from what the LLM produced.
3. **Provide the prompt** given to the LLM.

Whether to use an LLM depends on what you want out of the course. The process of creation — working
through a derivation, implementing an algorithm from scratch — is one of the best ways to learn.
Having an LLM create for you will likely limit what you take away.

### Privacy

Student data is protected under FERPA; see the
[Vanderbilt Student Privacy Statement](https://registrar.vanderbilt.edu/ferpa/vanderbilt-student-privacy-statement.php).
Please take care not to disclose private information during lectures or in submissions.

### Nondiscrimination and anti-harassment

Vanderbilt is committed to an environment free of discrimination and harassment of any kind. If you
feel you are being sexually harassed, please see [Project Safe](https://www.vanderbilt.edu/projectsafe/).
If you feel unsafe, taken advantage of in any way, or mentally or emotionally unwell, please reach
out to the [Student Care Network](https://www.vanderbilt.edu/studentcarenetwork/).

### Subject to change

Information in the course syllabus, other than the general assessment, may be subject to change
with advance notice, at the discretion of the instructor.

## 🌎 Previous Offerings and Related Courses

- [Vanderbilt — CS 6362, Fall 2024 (M. Berger)](https://matthewberger.github.io/teaching/aml/fall2024/)
- [Stanford — CS 236: Deep Generative Models](https://deepgenerativemodels.github.io/)
- [Berkeley — CS 294-158: Deep Unsupervised Learning](https://sites.google.com/view/berkeley-cs294-158-sp24/home)
- [CMU — 10-708: Probabilistic Graphical Models](https://www.cs.cmu.edu/~epxing/Class/10708-20/)
