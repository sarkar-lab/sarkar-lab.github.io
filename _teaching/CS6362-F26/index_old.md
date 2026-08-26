---
layout: page
title: CS6362 Advanced Machine Learning
term: Fall 2026
semester: Fall 2026
type: Graduate
category: Graduate
importance: 0        # lower = shows earlier
nav: false
published: false     # backup snapshot: shares index.md's permalink, so must not be output
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
fundamentals of **optimization** and **inference**; the second half builds on those foundations to
study supervised learning scenarios, generative models, and unsupervised learning.

<br><br>
<span style="color:#8e2de2;font-weight:600;">💡 The emphasis is on <i>why</i> these methods work — deriving them from first principles — so you can adapt and extend them, not only apply them.</span>

## Logistics

- **Course Code:** CS6362
- **Term:** Fall 2026
- **Class Times:** Mondays & Wednesdays <i>(time TBD)</i>
- **Location:** TBD
- **Instructor:** Hirak Sarkar
- **Office Hours:** TBD

## 🎯 Learning Goals

By the end of this course, students will be able to:

- **Analyze** gradient descent and its stochastic variants — why they work, and their limitations
- **Apply** specialized optimization methods: noise reduction, second-order methods, natural
  gradients, momentum, and the neural tangent kernel
- **Formulate** learning problems as Bayesian inference and reason about closed-form posteriors
- **Derive** and **implement** approximate inference — Laplace, variational inference, MCMC
- **Build** and **critique** generative models: VAEs, normalizing flows, score matching, diffusion
- **Quantify** predictive uncertainty and apply it to detection, adaptation, and data selection
- **Read** and **reconstruct** results from current machine learning research literature

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
  <td><a href="https://epubs.siam.org/doi/10.1137/16M1080173" class="paper-link">LSML</a> Sec. 2–4</td>
  <td></td>
</tr>
<tr>
  <td>Thu, Sep 03</td>
  <td></td>
  <td></td>
  <td><span class="due">Assignment 1 posted</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 3</b> (Sep 7) — Topics on gradient descent</td></tr>
<tr>
  <td>Mon, Sep 07</td>
  <td>Noise reduction</td>
  <td><a href="https://epubs.siam.org/doi/10.1137/16M1080173" class="paper-link">LSML</a> Sec. 5–7</td>
  <td></td>
</tr>
<tr>
  <td>Wed, Sep 09</td>
  <td>Neural tangent kernel</td>
  <td><a href="https://mml-book.github.io/" class="paper-link">MML</a> Ch. 12.4;
      <a href="https://arxiv.org/abs/1806.07572" class="paper-link">Neural tangent kernel</a>;
      <a href="https://arxiv.org/pdf/2006.10739" class="paper-link">Fourier features</a>;
      <a href="https://arxiv.org/abs/2305.12827" class="paper-link">Tangent space task arithmetic</a></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 4</b> (Sep 14) — Bayesian inference: basics, parametric and nonparametric methods</td></tr>
<tr>
  <td>Mon, Sep 14</td>
  <td>Bayesian statistics, linear regression</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 2.3, Ch. 3.2, Ch. 15.2.1–15.2.4</td>
  <td></td>
</tr>
<tr>
  <td>Wed, Sep 16</td>
  <td>Gaussian processes</td>
  <td><a href="https://gaussianprocess.org/gpml/chapters/" class="paper-link">GP</a> Ch. 2;
      <a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 3.7–3.8</td>
  <td></td>
</tr>
<tr>
  <td>Fri, Sep 18</td>
  <td></td>
  <td></td>
  <td><span class="due">Assignment 1 due</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 5</b> (Sep 21) — Approximate inference, variational inference</td></tr>
<tr>
  <td>Mon, Sep 21</td>
  <td>Model selection, Laplace approximation, information theory basics, ELBO</td>
  <td><a href="https://probml.github.io/pml-book/book1.html" class="paper-link">PML-1</a> Ch. 6.1–6.2;
      <a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 5.1, Ch. 7.4, Ch. 10.1</td>
  <td><span class="due">Assignment 2 posted</span></td>
</tr>
<tr>
  <td>Wed, Sep 23</td>
  <td>Gradient-based variational inference</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 6.3.5, Ch. 10.2;
      <a href="https://www.jmlr.org/papers/volume21/19-346/19-346.pdf" class="paper-link">MCGE</a></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 6</b> (Sep 28) — Variational inference, MCMC</td></tr>
<tr>
  <td>Mon, Sep 28</td>
  <td>Variational inference continued</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 6.3.5, Ch. 10.2;
      <a href="https://www.jmlr.org/papers/volume21/19-346/19-346.pdf" class="paper-link">MCGE</a></td>
  <td></td>
</tr>
<tr>
  <td>Wed, Sep 30</td>
  <td>Monte Carlo, Markov chains</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 11.1–11.4, Ch. 12.1–12.2</td>
  <td></td>
</tr>
<tr>
  <td>Fri, Oct 02</td>
  <td></td>
  <td></td>
  <td><span class="due">Assignment 2 due</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 7</b> (Oct 5) — Project introductions, midterm</td></tr>
<tr>
  <td>Mon, Oct 05</td>
  <td>Project introductions</td>
  <td></td>
  <td><span class="due">Proposal presentations</span></td>
</tr>
<tr>
  <td>Wed, Oct 07</td>
  <td><b>Midterm</b></td>
  <td></td>
  <td><span class="due">Will be graded</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 8</b> (Oct 12) — MCMC</td></tr>
<tr>
  <td>Mon, Oct 12</td>
  <td>MCMC: Metropolis–Hastings, Gibbs sampling, mixture models</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 12.1–12.3, 12.5</td>
  <td></td>
</tr>
<tr>
  <td>Wed, Oct 14</td>
  <td>Gibbs sampling continued, HMC</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 17.1–17.4</td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 9</b> (Oct 19) — Bayesian neural networks, domain adaptation</td></tr>
<tr>
  <td>Mon, Oct 19</td>
  <td>Bayesian neural networks</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 17.1–17.4</td>
  <td><span class="due">Assignment 3 posted</span></td>
</tr>
<tr>
  <td>Wed, Oct 21</td>
  <td>Out-of-distribution detection, domain adaptation</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 19.1–19.7</td>
  <td></td>
</tr>
<tr>
  <td>Thu–Fri, Oct 22–23</td>
  <td><b>No class — Fall Break</b></td>
  <td></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 10</b> (Oct 26) — Active learning, few-shot learning</td></tr>
<tr>
  <td>Mon, Oct 26</td>
  <td>(Bayesian) Active learning</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 34.7;
      <a href="http://mlg.eng.cam.ac.uk/pub/pdf/HouHusGha11a.pdf" class="paper-link">Bayesian active learning</a>;
      <a href="https://proceedings.mlr.press/v70/gal17a/gal17a.pdf" class="paper-link">Deep Bayesian Active Learning</a></td>
  <td></td>
</tr>
<tr>
  <td>Wed, Oct 28</td>
  <td>Few-shot learning</td>
  <td><a href="https://arxiv.org/pdf/1703.03400" class="paper-link">MAML</a>;
      <a href="https://openaccess.thecvf.com/content_cvpr_2018/papers/Sung_Learning_to_Compare_CVPR_2018_paper.pdf" class="paper-link">Learning to compare</a>;
      <a href="https://arxiv.org/pdf/1909.09157" class="paper-link">ANIL</a></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 11</b> (Nov 2) — Generative models: variational autoencoders</td></tr>
<tr>
  <td>Mon, Nov 02</td>
  <td>Variational autoencoders: basics, posterior collapse</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 21.1–21.2, 21.4</td>
  <td><span class="due">Assignment 3 due</span></td>
</tr>
<tr>
  <td>Wed, Nov 04</td>
  <td>Variational autoencoders: disentanglement, discrete latents</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 21.3, 21.5–21.6</td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 12</b> (Nov 9) — Generative models: normalizing flows</td></tr>
<tr>
  <td>Mon, Nov 09</td>
  <td>Normalizing flows: basics, discrete flows</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 23</td>
  <td></td>
</tr>
<tr>
  <td>Wed, Nov 11</td>
  <td>Normalizing flows: continuous-time flows</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 23</td>
  <td></td>
</tr>
<tr>
  <td>Fri, Nov 13</td>
  <td></td>
  <td></td>
  <td><span class="due">Project midway report due</span></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 13</b> (Nov 16) — Generative models: score matching, diffusion models</td></tr>
<tr>
  <td>Mon, Nov 16</td>
  <td>Energy-based models</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 24</td>
  <td></td>
</tr>
<tr>
  <td>Wed, Nov 18</td>
  <td>Diffusion models</td>
  <td><a href="https://probml.github.io/pml-book/book2.html" class="paper-link">PML-2</a> Ch. 25</td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 14</b> (Nov 21–29) — Thanksgiving holidays</td></tr>
<tr>
  <td>Nov 21–29</td>
  <td><b>No class — Thanksgiving holidays</b></td>
  <td></td>
  <td></td>
</tr>

<tr class="wk"><td colspan="4"><b>Week 15</b> (Nov 30) — Unsupervised learning</td></tr>
<tr>
  <td>Mon, Nov 30</td>
  <td>Latent factor analysis</td>
  <td></td>
  <td></td>
</tr>
<tr>
  <td>Wed, Dec 02</td>
  <td>Project discussions</td>
  <td></td>
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

## 🧩 Topics Covered

**1. Fundamentals of optimization** — finding the *best* model parameters in supervised learning.
Stochastic gradient descent is emphasized given its predominance in modern ML: what gradient
descent is, why it works, and its limitations, together with the necessary linear algebra,
probability & statistics, and convexity. Then specialized topics: noise reduction methods,
second-order methods, natural gradients, momentum, and — specific to neural networks — the neural
tangent kernel.

**2. Fundamentals of inference** — finding a *set* of models rather than one. Bayesian inference
and the posterior over model parameters, starting with closed-form cases: basics of Bayesian
statistics, parametric models (working with Gaussians and friends), nonparametric models (Gaussian
processes), and model selection. Then the practical case where the posterior is intractable —
**approximate inference**: Laplace approximation, variational inference, Markov chain Monte Carlo,
and neural network posteriors.

**3. Supervised learning scenarios** — organized by data characteristics: domain adaptation and
out-of-distribution detection, active learning, few-shot learning, semi-supervised learning.

**4. Generation** — variational autoencoders, normalizing flows, score matching, diffusion models.

**5. Unsupervised learning** — factor analysis methods, topic modeling, and dimensionality
reduction (tSNE, UMAP).

## 🏗️ Course Format

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

## 👥 Course Assessment

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

### Grade scale

97+ : A+ &nbsp;·&nbsp; 94–97 : A &nbsp;·&nbsp; 90–94 : A− &nbsp;·&nbsp; 87–90 : B+ &nbsp;·&nbsp;
84–87 : B &nbsp;·&nbsp; 80–84 : B− &nbsp;·&nbsp; 77–80 : C+ &nbsp;·&nbsp; 74–77 : C &nbsp;·&nbsp;
70–74 : C− &nbsp;·&nbsp; 67–70 : D+ &nbsp;·&nbsp; 64–67 : D &nbsp;·&nbsp; 60–64 : D− &nbsp;·&nbsp;
&lt; 60 : F

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
- [**LSML**](https://epubs.siam.org/doi/10.1137/16M1080173) — Bottou, Curtis & Nocedal, *Optimization Methods for Large-Scale Machine Learning*

**Inference**

- [**PML-1**](https://probml.github.io/pml-book/book1.html) — Murphy, *Probabilistic Machine Learning: An Introduction*
- [**PML-2**](https://probml.github.io/pml-book/book2.html) — Murphy, *Probabilistic Machine Learning: Advanced Topics*
- [**GP**](https://gaussianprocess.org/gpml/chapters/) — Rasmussen & Williams, *Gaussian Processes for Machine Learning*
- [**MCGE**](https://www.jmlr.org/papers/volume21/19-346/19-346.pdf) — Mohamed, Rosca, Figurnov & Mnih, *Monte Carlo Gradient Estimation in Machine Learning*

The readings listed in the schedule are intended to **complement** the lecture slides.

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
