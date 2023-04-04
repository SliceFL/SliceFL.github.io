---
permalink: /techniques/
layout: single

title: "Techniques"
toc: true
toc_label: "Content"
toc_icon: "cog"
toc_sticky: true
header:
  overlay_image: /assets/images/deszka.jpg

---
# Advanced Techniques

{% assign entries_layout = page.entries_layout | default: 'list' %}
{% for post in site.posts %}
{% if post.categories contains "Advanced"%}
<section id="Advanced" class="taxonomy__section">
    <div class="entries-{{ entries_layout }}">
        {% include archive-single.html type=entries_layout %}... Click on the title for more details. 
    </div>
    <a href="#page-title" class="back-to-top">{{ site.data.ui-text[site.locale].back_to_top | default: 'Back to Top' }} &uarr;</a>
  </section>
{%endif%}
{% endfor %}

# Fundamentals

{% assign entries_layout = page.entries_layout | default: 'list' %}
{% for post in site.posts reversed %}
{% if post.categories contains "Fundamentals"%}
<section id="Fundamentals" class="taxonomy__section">
    <div class="entries-{{ entries_layout }}">
    {% include archive-single.html type=entries_layout %}... Click on the title for more details. 
      </div>
      <a href="#page-title" class="back-to-top">{{ site.data.ui-text[site.locale].back_to_top | default: 'Back to Top' }} &uarr;</a>
  </section>
{%endif%}
{% endfor %}

