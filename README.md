# Erd-s-Problem-272-An-Independent-Proof-with-an-Explicit-Threshold

Independently obtained results on the exact extremal value in [Erdős Problem #272](https://www.erdosproblems.com/272), with a current explicit threshold of **$N>4000$**.

The main result recorded here is
$$
t(N)=\binom{N}{2}+1+\left\lfloor\frac{N-1}{4}\right\rfloor
\qquad\text{for every integer }N>4000.
$$

**Status:** research in progress. The result and research chronology below are reported by the author. The proof manuscript and supporting materials are being prepared for publication; this initial README does not assert independent verification or a completed Lean formalization.

## Problem and main result

Write $[N]=\{1,\ldots,N\}$. A family $\mathcal F\subseteq\mathcal P([N])$ is admissible if, for every two distinct members $A,B\in\mathcal F$, the intersection $A\cap B$ is a nonempty arithmetic progression. Singletons and two-element sets count as arithmetic progressions. Members of $\mathcal F$ may be arbitrary subsets of $[N]$.

Define
$$
t(N)=\max\{|\mathcal F|:\mathcal F\text{ is admissible on }[N]\},
\qquad
B(N)=\binom{N}{2}+1+\left\lfloor\frac{N-1}{4}\right\rfloor.
$$

**Main result.** For every integer $N>4000$, every admissible family on $[N]$ satisfies
$$
|\mathcal F|\le B(N).
$$
Together with Szabó's matching construction, this gives $t(N)=B(N)$ throughout that range.

The upper bound applies to all admissible families, with no assumption that their members share a common element. The threshold is strict: **$N>4000$, equivalently $N\ge4001$**.

This result covers the entire infinite tail above 4000. It does not by itself establish the exact formula for every positive integer $N$; the range $1\le N\le4000$ requires separate treatment.

## Independent discovery

I obtained the eventual exact-value result independently on **24 October 2026** and subsequently reduced the explicit threshold to **$N>4000$ on 1 November 2026**. This work was developed independently of Li Xiang's related draft dated 30 October 2026.

The earlier stages of my work were not publicly posted at the time. The chronology below records when I obtained the results; public release dates are recorded separately. I acknowledge the related public work below and make no claim here to first-publication priority.

## Relation to existing work

The following comparison concerns mathematical statements and their ranges. It does not attribute proof methods or establish discovery priority. External results are summarized from the linked papers and author submissions.

| Work | Result and scope | Relation to this project |
| --- | --- | --- |
| Szabó's construction, reproduced in [Yang, Theorem 1.2](https://arxiv.org/html/2607.23004v1) | $t(N)\ge B(N)$ for every $N\ge1$. | Supplies the known matching lower bound. This project claims no novelty for that construction. |
| [Zhanfu Yang, arXiv:2607.23004v1](https://arxiv.org/abs/2607.23004v1), submitted 25 July 2026 | Reports the exact maximum $B(N)$ for families sharing a common element, for every $N\ge1$, and unrestricted exact values for $3\le N\le12$. | The present large-$N$ statement has no common-element assumption. Yang's common-element result also covers smaller $N$, so the two scopes should be distinguished. |
| [Jensen Kohlmeyer and Liam Kruer, *A linear error bound for Erdős problem 272*](https://github.com/TheJustinSunPrize/awards/issues/4923) | Reports $t(N)=N^2/2+O(N)$ without a common-element assumption. The link identifies the manuscript and its stated scope. | The present statement specifies the exact value for each $N>4000$. |
| [Li Xiang, *The exact maximum in Erdős problem 272 for sufficiently large ground sets*](https://github.com/TheJustinSunPrize/awards/pull/5513) | Paper dated 30 October 2026; prize-repository PR opened 31 October. The draft reports $t(N)=B(N)$ for every $N\ge642498$, with a simpler paper route for $N\ge2^{49}$. | The unrestricted exact formula was obtained independently in this project, with the current smaller threshold $N>4000$. |

Li Xiang's submission pins the proof repository [lixiang90/Erdos272 at commit d5dc0e6](https://github.com/lixiang90/Erdos272/tree/d5dc0e6dbaaa954f8d89b05f72ed25cf6722be82). As of 1 November 2026, PR #5513 is a draft and explicitly does not claim organizer acceptance or independent human review.

Relative to that draft's stated range, the result recorded here additionally covers every integer
$$
4001\le N<642498.
$$
The smaller threshold is a comparison of stated theorem ranges. This work was obtained independently of that draft.

## Research chronology

The following table records my independent research and the successive explicit thresholds. These are dates of research progress, distinct from the dates when proof artifacts become publicly available.

| Date | Milestone | Range reported at that stage |
| --- | --- | --- |
| 24 October 2026 | Eventual exact-value theorem, route P062 | $N\ge2^{252}$ |
| 24 October 2026 | Alternative eventual proof, route P057 | $N\ge2^{2048}$ |
| 25 October 2026 | Improved global threshold, P082 | $N\ge2^{90}$ |
| 29 October 2026 | Improved explicit threshold | $N\ge75000$ |
| 30 October 2026 | Further threshold improvement | $N\ge49000$ |
| 1 November 2026 | Current threshold | $N>4000$ |

The dates in this table are my account of the research chronology. Public release dates and fixed proof versions will be recorded separately as materials are published.

I retain ChatGPT conversation records, including their platform-recorded timestamps, as supporting documentation for this research chronology.

The records and this repository are currently private; these dates describe research progress, not public disclosure. The first public release date will be recorded when the repository is made public.

## Proof materials and next steps

The initial repository description records the precise theorem, its scope, related work, and the research chronology. The next publication steps are:

- Publish the complete manuscript, including every hypothesis and the proof of the 4000 threshold.
- Identify proof dependencies and distinguish any computation from the mathematical argument.
- Provide reproducible verification instructions for any computational or formal components that are released.
- Track the remaining finite range separately from the large-$N$ theorem.

Questions, corrections, and independent checks are welcome through GitHub issues. Please identify the statement, proof step, or version under discussion.
