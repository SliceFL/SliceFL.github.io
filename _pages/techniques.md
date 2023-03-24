---
permalink: /techniques/
title: "Techniques"
toc: true
toc_label: "Content"
toc_icon: "cog"
toc_sticky: true
header:
  overlay_image: /assets/images/deszka.jpg
---

### Program Slicing

Program slicing is a software engineering technique that aims to isolate parts of a program that are relevant to a specific task. By "slicing" away unneeded parts of the code, it can help programmers better understand the relationships between different parts of a program, and make it easier to identify and fix bugs or optimize the performance of the code. The slices produced by program slicing can be either dynamic or static, depending on whether they are based on the actual execution of the program or on a static analysis of the code. Program slicing has many advantages, such as reducing the amount of code that needs to be examined, making it easier to understand the logic of a program, and increasing the efficiency of debugging. However, there are also some disadvantages to program slicing, such as the need for specialized tools, limitations in terms of the types of programs that can be sliced, and the need for accurate and up-to-date data about the program. For more information, please visit [this page]({% link _pages/slicing.md %}){: .btn .btn--info}

### Spectrum-based Fault Localization

Spectrum-based fault localization (SBFL) is a technique for identifying the source of faults in software systems by analyzing the frequency of test cases that fail and pass. It is based on the hypothesis that the root cause of a fault is likely to be the component that has the highest number of failing test cases. SBFL has been widely used in software debugging and has been shown to be effective in reducing the search space for faults. In SBFL, the program is divided into smaller units or components, and the results of running test cases on these components are used to compute a fault score for each component. The component with the highest fault score is considered to be the most likely location of the fault. SBFL is widely adopted due to its simplicity, efficiency, and accuracy compared to other fault localization techniques.
For more information, please visit [this page]({% link _pages/sbfl.md %}){: .btn .btn--info}