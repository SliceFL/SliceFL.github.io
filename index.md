---
title: "Homepage of the SliceFL project"
author_profile: true
toc: true
toc_label: "Content"
toc_icon: "cog"
layout: single
toc_sticky: true

carousels:
  - images: 
    - image: /assets/images/slideshow/pic1.PNG
    - image: /assets/images/slideshow/pic2.PNG
    - image: /assets/images/slideshow/pic3.PNG
    - image: /assets/images/slideshow/pic4.PNG
    - image: /assets/images/slideshow/pic5.PNG
    - image: /assets/images/slideshow/pic6.PNG
    - image: /assets/images/slideshow/pic7.PNG
    - image: /assets/images/slideshow/pic8.PNG
    - image: /assets/images/slideshow/pic9.PNG
    - image: /assets/images/slideshow/pic91.PNG    
---


{% include carousel.html height="50" unit="%" duration="5" number="1" %}


## The Slice-FL appears

With the Slice-Fl project, we aim to have an automatic debugging method that can effectively help developers in real-world situations. To this end, we combine classical SBFL and dynamic backward slicing, exploiting the positive features of both while minimizing their drawbacks. We achieve this by replacing the hit-based coverage matrix with a slicing basis, i.e., starting from the assert statements in the tests, we compute the sets of statements that affect the assert's output. The advantage of this method is, among others, that the slice, since it does not contain instructions whose execution is irrelevant to the result, leads to a smaller and more accurate matrix.
