---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

### [The Design and Implementation of Venbrace, a Text Language for App Inventor](https://repository.wellesley.edu/object/ir1232)

This undergraduate thesis details the design, implementation, and evaluation (through a user study) of Venbrace, a fully-braced textual syntax for App Inventor that aims to improve the usability of the blocks-based programming environment.

Recommended citation: R. Huang. The Design and Implementation of Venbrace, a Text Language for App Inventor (Bachelor's thesis). Retrieved from [https://repository.wellesley.edu/object/ir1232](https://repository.wellesley.edu/object/ir1232).

### [A Design for Bidirectional Conversion between Blocks and Text for App Inventor](https://ieeexplore.ieee.org/document/8941197)

_Poster presented in IEEE Blocks and Beyond Workshop, 2019_

This poster presents a preliminary design for Venbrace based on a collection of design principles.

Recommended citation: R. Huang and F. Turbak, "A Design for Bidirectional Conversion between Blocks and Text for App Inventor," 2019 IEEE Blocks and Beyond Workshop (B&B), Memphis, TN, USA, 2019, pp. 87-89, doi: [10.1109/BB48857.2019.8941197.](10.1109/BB48857.2019.8941197.)

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
  {% include base_path %}

  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}


