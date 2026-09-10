# Course Sources

## Scope and provenance

Initial source review: 2026-09-10. Authority order: explicit user instructions; supplied course lectures and assignments; relevant study discussions; minimal mathematical definitions needed to express already-discussed ideas. The typed 2026 Lecture 1–2 files give the precise section and equation references used here. Definitions added for readability are explanatory scaffolding, not invented lecture quotations.

The repository stores plain Markdown conceptual notes, not source-PDF copies, instructor solutions or transcripts. Source filenames below identify the project attachments; they are not nonexistent vault attachment links. PDF page numbers mean physical pages in the uploaded file, not the footer's cumulative page count.

## Lecture 1

Source: `lec01-2026_v1.pdf`, 9 PDF pages, Nils Deppe, PHYS-6561. PDF pp. 1–3 are a broad table of contents, **not** evidence that the entire course has already been taught or discussed.

| Location | Course material | Vault use |
| --- | --- | --- |
| PDF pp. 4–5; §1.1; eqs. (1)–(18) | Units and constants; Gaussian choice | [[Gaussian units and the 1 over c factors]] |
| PDF p. 6; §§1.2–1.4; eqs. (19)–(29) | Microscopic and macroscopic Maxwell equations; linear media | [[Maxwell equations]] |
| PDF p. 7; §1.5; eqs. (32)–(33) | Lorentz force and particle power | [[Lorentz force]]; [[Work and J dot E]] |
| PDF pp. 7–8; §1.6; eqs. (34)–(42) | Energy balance, $u$, $\mathbf S$ | [[Current density]]; [[Poynting theorem]]; [[Electromagnetic energy density]]; [[Poynting vector]] |
| PDF pp. 8–9; §1.7; eqs. (43)–(58) | Cartesian tensors, rotations, outer products | [[Rank-2 tensors and outer products]] |
| PDF p. 9; §1.8; eqs. (59)–(61) | Beginning of momentum conservation | [[Maxwell stress tensor]] |

The file explicitly marks the end of Lecture 1 after eq. (61).

## Lecture 2

Source: `lec02-2026_v1.pdf`, 5 PDF pages, Nils Deppe, PHYS-6561.

| Location | Course material | Vault use |
| --- | --- | --- |
| PDF pp. 1–2; §1.8 continuation; eqs. (62)–(79) | Field momentum and Maxwell stress | [[Maxwell stress tensor]] |
| PDF pp. 2–3; §§1.9–1.10 | Angular momentum; macroscopic conservation | Scope boundary; no separate notes yet |
| PDF p. 3; §2.1; eqs. (91)–(100) | Potentials, including $\mathbf B=\nabla\times\mathbf A$ | Prerequisite pointer in [[Homework/HW1 Map#Problem 1a|HW1 1(a)]] only |
| PDF pp. 4–5; §2.2 | Lorenz and Coulomb gauges | Pointer for HW1's magnetostatic setup; no full gauge/Green-function lesson |

The file explicitly marks the end of Lecture 2 after eq. (113).

## Homework sources

- `Homework0.pdf`: 5 pages, explicitly **Fall 2026**. Problem 1 begins on PDF p. 1; problem 2 begins on p. 2 with its equation on p. 3; problem 3 spans pp. 3–4. Page 5 finishes contextual examples. Mapped in [[Homework/HW0 Map]].
- `Homework1.pdf`: 1 page, explicitly **Fall 2025** in its header. The user supplied it for this course; its three problems are mapped in [[Homework/HW1 Map]]. Whether the header is stale or this is a previous-year assignment has not been independently established.
- `Homework1_solns.pdf`, HW2–HW6 and the other supplied solution PDFs were not used to generate solved answers or extend this initial set.
- `AllNotes.pdf`: 145-page handwritten compilation. Text extraction is unreliable. It was inventoried, but not used to claim exact lecture coverage or equations; the legible typed 2026 files are the source for this initial pass. Relevant pages can be inspected visually in future study sessions.

## Syllabus

Source: `Syllabus-7.pdf`, 3 pages. PDF p. 1 identifies lectures as primary course material and textbooks as supplements. It lists spherical harmonics among useful prerequisites. Homework is 5%, the prelim 40%, and the final 55%; homework self-grading is required. The syllabus requires completing and self-grading all but two assignments for final-exam eligibility and acknowledging assistance. Homework maps should track understanding and self-grading without implying that writing a map completes either requirement.

This vault does not infer due dates from an undated assignment PDF or claim a submission is complete based on an unrelated earlier conversation.

## Study-discussion evidence

Preserved learning questions include divergence versus curl, spatial-derivative units, the Gaussian $1/c$ factors, $\mathbf J=\sigma\mathbf E$, density versus flux, matter's separate energy store, steady field energy with energy transfer, stress-tensor directional slots, and orthogonal versus orthonormal versus complete. The stress/spiraling misconception is explicitly supplied by the user in the vault request. The water-jar analogy and equal-inflow/outflow statement are visible in project conversation context.

Basic Legendre and spherical-harmonic definitions support the named discussion topics and HW0. No exact lecture section for their full derivation was verified in the typed sources, so their notes say so. Generic teaching examples are labeled examples rather than attributed as things the user previously said.

## Clarifications retained with the source

1. **Lecture 1, eq. (41), PDF p. 8:** with outward $\mathbf n$, $\oint\mathbf S\cdot\mathbf n\,dA$ is outward energy flow. The negative appearing in the balance is inward supply. The adjacent prose calling the integral “into” the volume is ambiguous; the equation fixes the sign. The volume-to-surface step is the divergence theorem.
2. **Lecture 2, eq. (79), PDF p. 2:** static fields remove $d\mathbf p_{\rm field}/dt$. They do not alone imply zero electromagnetic force. The retained usable relation is $\mathbf F_{\rm EM}=\oint T\cdot\mathbf n\,dA$. Any further zero requires additional conditions. Mechanical supports can balance a nonzero electromagnetic force.
3. **Lecture 2, eqs. (73), (76), (78):** the displayed stress convention gives $f_i=\partial_jT_{ij}-\partial_tg_i$. Therefore the outward field-momentum-flux tensor in a continuity form is $-T$. The notes distinguish this from traction $T\cdot\mathbf n$ instead of changing the lecture's definition of $T$.
4. **HW0 1(c), PDF p. 1:** the target is written $e^{-ax}$ but the interval label is $q\in[0,2\pi]$. The map treats $x$ as the intended interval variable and marks that reading; it does not silently alter the source.

These are narrow reading/consistency clarifications, not replacements for the supplied course material.
