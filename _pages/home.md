---

permalink: /home/
title: "Homepage of the Slice-FL project"
author_profile: true
toc: true
toc_label: "Content"
toc_icon: "cog"
---

## The fate of the developer

As we know well since Murphy, *what can go wrong, will go wrong*. This applies to software programs as well, and finding bugs can be a challenging and time-consuming task, not to mention that fixing one issue often leads to the discovery of several others. Over the years, various automated methods have been developed to tackle this problem, such as coverage-based SBFL and program slicing. However, these methods are more theoretical than practical, as the former is fast but inaccurate, while the latter is accurate but too expensive to use.

## The Slice-FL appears

With the Slice-Fl project, we aim to have an automatic debugging method that can effectively help developers in real-world situations. To this end, we combine classical SBFL and dynamic backward slicing, exploiting the positive features of both while minimizing their drawbacks. We achieve this by replacing the hit-based coverage matrix with a slicing basis, i.e., starting from the assert statements in the tests, we compute the sets of statements that affect the assert's output. The advantage of this method is, among others, that the slice, since it does not contain instructions whose execution is irrelevant to the result, leads to a smaller and more accurate matrix.