---
title: Get Involved
permalink: /get-involved/
class: get-involved
layout: default

# full span, top of page section
hero:
  text: Get Involved
  subtext: Join our community of innovators working to turn federal open data into technologies that solve real-world problems for people across the country.

# connecting-banner-with-subheader-inverse.html
banner-subheader-inverse:
  top:
    background: base-darkest
    line: '-light'
  bottom:
    background: white

content-light:
  title: Participate in TOP
  skip-top-border: true
  skip-bottom-border: true
  body: Sprints are 12-week product development cycles where we bring together tech teams and collaborators to build digital products using open data.
  right-col: participate-right.md

join:
  title: Stay in the Loop
  skip-top-border: true
  skip-bottom-border: true
  right-col: in-the-loop-right.md

callout:
  text: Win Funding to Scale Your Technology
  id: prize-challenge
  markdownSrc: prize-callout.md

---
{% include hero.html %}
{% include connecting-banner-with-subheader-inverse.html %}

{% capture left-col %}
  {% include image.html src="photos/get-involved/stickies.jpg" alt="Image of a man at a table with sticky notes" %}
{% endcapture %}
{% capture right-col %}
  {% include_relative {{ page.content-light.right-col }} %}
{% endcapture %}
{% include two-column-markdown.html content=page.content-light left-col=left-col%}

{% include text-callout-centered.html content=page.callout %}

{% capture left-join %}
  {% include image.html src="photos/get-involved/arrow.jpg" alt="Illustration of an arrow pointing to the right over a navy blue field" %}
{% endcapture %}
{% capture right-join %}
  {% include_relative {{ page.join.right-col }} %}
{% endcapture %}
{% include two-column-markdown.html content=page.join left-col=left-join right-col=right-join %}
