# Erdős Problem 272

English** | [简体中文](README.zh-CN.md)

**Peihan Wu**

This repository presents my research manuscript on [Erdős Problem 272](https://www.erdosproblems.com/272). The manuscript claims that, for every integer $N\ge4000$,

$$
t(N)=\binom N2+1+\left\lfloor\frac{N-1}{4}\right\rfloor.
$$

Here $t(N)$ is the maximum size of a family of distinct subsets of $[N]=\{1,\ldots,N\}$ whose intersections of distinct members are nonempty arithmetic progressions. Singletons and pairs count as arithmetic progressions. Members themselves need not be progressions, and no common point is assumed. The stated range includes $N=4000$; the manuscript does not claim to settle all smaller parameters or classify every extremal family.

## Paper and public materials

[Read the English paper (PDF)](erdos272_arxiv_en.pdf)

This repository currently publishes only the paper PDF and the English and Chinese READMEs. Code, computational certificates, technical source notes and Lean files are not distributed here. The paper still relies on electronic mathematical supplements and computational certificates, so the files currently public in this repository do not suffice to reproduce all computations or verify the entire chain of technical dependencies independently.

## Independent research declaration

**I declare that I conducted and completed this research independently, without research dependence on Li Xiang's draft. That draft was not the source of my arguments or threshold improvements, and this research is not a continuation, adaptation or joint development of it.** Citations to that draft serve only to describe the publicly reported scope of concurrent work.

This declaration concerns my threshold-improvement research. Szabó's existing construction and the published results and methods of Yang and other authors retain their attribution in the paper. GPT assistance in research and review is disclosed below.

## Research timeline

The table records only the $N$ thresholds in my research records. These dates are distinct from first public disclosure and from completion of verification of each version.

| Date | $N$ threshold |
| --- | --- |
| 2026-10-24 | $N\ge2^{252}$ |
| 2026-10-25 | $N\ge2^{90}$ |
| 2026-10-29 | $N\ge75000$ |
| 2026-10-30 | $N\ge49000$ |
| 2026-11-01 | $N\ge4000$ |

## Relationship to earlier work

Szabó supplied the matching lower-bound construction used here. [Zhanfu Yang's preprint](https://arxiv.org/abs/2607.23004v1) treats the common-point case, private pairs and staircase counting, and reports exact values for $3\le N\le12$. [Jensen Kohlmeyer and Liam Kruer](https://github.com/TheJustinSunPrize/awards/issues/4923) reported a linear error bound.

[Li Xiang's draft dated October 30, 2026, and its submission record](https://github.com/TheJustinSunPrize/awards/pull/5513) report the exact formula for $N\ge642498$. This manuscript claims the range $N\ge4000$. This comparison of ranges does not indicate that my research derives from that draft and does not adjudicate discovery priority. Detailed references and attribution appear in the paper.

## Difficulties below 4000 and limitations of the method

Further lowering the threshold below 4000 has remained difficult in my research. After extended work, I have only obtained further drafts concerning the 3800–4000 range. These drafts are not part of the current paper's result, and this repository does not claim a threshold of 3800.

In the present method, as $N$ grows, the gains supplied by structural restrictions can increasingly dominate boundary contributions, exceptional configurations and estimation errors. As $N$ becomes smaller, those losses occupy a larger share of the available margin, requiring finer structural estimates. Obtaining such estimates has proved difficult in my work.

I expect this structural-estimate approach may encounter substantial obstacles when $N$ is in the tens to hundreds. This is my assessment of the current method, rather than a theorem that small parameters are intrinsically harder or that the approach cannot be improved. Further progress may require new structural ideas, a more precise treatment of exceptions, or a different rigorous computational approach.

## Lean formalization and GPT-assisted review

Some Lean formalization has been completed, and the unfinished project remains work in progress. I am also considering whether to continue this route; I do not currently commit to completing a full formalization or to a completion date. The partial work has not been made public and is not used to justify any step of the present paper.

The manuscript has undergone GPT-assisted review of its arguments, dependency chain, citations and presentation. GPT also assisted with mathematical exploration, proof reconstruction and gap repair, implementation and manuscript preparation. This review is a tool-assisted check, not independent human peer review, complete proof-assistant verification or certification of correctness. The named human author remains responsible for the paper's contents.

## Collaboration, attribution and the Justin Sun Prize

This work concerns [JSP-000233](https://github.com/TheJustinSunPrize/awards/blob/main/problems/catalog-0201-0300.md#JSP-000233) and presents partial research results towards the original problem. Specific questions about the manuscript, research on the remaining parameters, independent checking and formalization contributions are welcome.

**If a later complete solution or prize submission materially relies on my results, please cite the specific statements and fixed version, identify my actual contribution alongside those of earlier authors and other contributors, and contact me through a GitHub issue. I would like to coordinate accurate attribution and discuss participation in a future joint application for qualifying contributions. Joint application roles, authorship and any proposed prize allocation should be discussed explicitly in advance, according to actual contributions and applicable rules.**

This repository claims no accepted complete solution, full public Lean proof of the original problem, award decision or automatic prize share. Eligibility and recognition are governed by the organizer's [award process](https://github.com/TheJustinSunPrize/awards/blob/main/docs/award-process.md) and [attribution policy](https://github.com/TheJustinSunPrize/awards/blob/main/docs/attribution.md).


