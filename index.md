---
title: "Homepage of the SliceFL Project"
author_profile: true
toc: true
toc_label: "Content"
toc_icon: "cog"
layout: single
toc_sticky: true

carousels:
  - images: 
    - image: /assets/images/slide_show/pic1.png
    - image: /assets/images/slide_show/pic2.png
    - image: /assets/images/slide_show/pic3.png
    - image: /assets/images/slide_show/pic4.png
    - image: /assets/images/slide_show/pic5.png
    - image: /assets/images/slide_show/pic6.png
    - image: /assets/images/slide_show/pic7.png
    - image: /assets/images/slide_show/pic8.png
    - image: /assets/images/slide_show/pic9.png
    - image: /assets/images/slide_show/pic91.png    
---


{% include carousel.html height="50" unit="%" duration="5" number="1" %}


## The SliceFL project

In the SliceFL project, we conduct research on automated debugging methods that can effectively help developers in real-world situations. Our aim is to develop techniques based on state-of-the-art research achievements but which are robust and efficient enough to be attractive for the developers.

Our current focus is on two popular techniques proposed for automated debugging, **program slicing** and automated **fault localization**. With slicing, code elements contributing to the computation at the fault can be determined, while fault localization aims at narrowing down the most probable faulty elements based on test outcomes. We combine the two techniques, exploiting the positive features of both while minimizing their drawbacks. Currently, we experiment with Spectrum-Based Fault Localization (SBFL) and Backward Dynamic Program Slicing that work on program code and associated unit tests. Starting from the asserts in the tests, we compute the slices which contain statements that affect the assert’s output, and then we use this information in the spectrum matrix required by SBFL. Traditionally, SBFL matrix is based on simple code coverage, and we show why slices are much better for this purpose.

Developing tools to efficiently compute precise-enough program slices which can be used in SBFL, and integrating them in popular IDE-s is our short-term goal in the SliceFL project. Pages of this website include details of the techniques, publications and related resources, and possibilities for contributing to this effort.