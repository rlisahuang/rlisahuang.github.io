---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---
<!-- ### [Improving the Teaching and Learning of Symbolic Logic Solving via the Web](/publications/)

**Ruanqianqian (Lisa) Huang**, Ayana Monroe, Sorin Lerner, Peli de Halleux and Nikolaj Bjørner. In preparation. -->

### [Visualizing Code-Behavior Correspondences in Event-Driven Programming](/publications/)

**Ruanqianqian (Lisa) Huang** and Sorin Lerner. In submission.

<h3><a href="/files/plateau_23.pdf" target="_blank">How do Haskell programmers debug?</a></h3>

**Ruanqianqian (Lisa) Huang**, Elizaveta Pertseva, Michael Coblenz, and Sorin Lerner. To appear in _the 13th annual workshop on the intersection of HCI and PL (PLATEAU '23)_.

<h3><a href="/files/research_exam_report.pdf" target="_blank">Towards Live Programming for Interactive GUI Applications</a></h3>

**Ruanqianqian (Lisa) Huang**. 2022. Research Exam. UC San Diego.

<h3><a href="/files/PB4Edu_SIGCSE22.pdf" target="_blank">Investigating the Impact of Using a Live Programming Environment in a CS1 Course</a></h3>

**Ruanqianqian (Lisa) Huang**, Kasra Ferdowsi, Ana Selvaraj, Adalbert Gerald Soosai Raj, and Sorin Lerner. In _Proceedings of the 53rd ACM Technical Symposium on Computer Science Education (SIGCSE ’22)_, Providence, RI, USA, 2022.

<h3><a href="https://repository.wellesley.edu/object/ir1232" target="_blank">The Design and Implementation of Venbrace, a Text Language for App Inventor</a></h3>

**Ruanqianqian Huang**. 2020. Bachelor's Thesis. Wellesley College.

<!-- This undergraduate thesis details the design, implementation, and evaluation (through a user study) of Venbrace, a fully-braced textual syntax for App Inventor that aims to improve the usability of the blocks-based programming environment. -->

<!-- R. Huang. The Design and Implementation of Venbrace, a Text Language for App Inventor (Bachelor's thesis). Retrieved from [https://repository.wellesley.edu/object/ir1232](https://repository.wellesley.edu/object/ir1232). -->

<h3><a href="https://ieeexplore.ieee.org/document/8941197" target="_blank">A Design for Bidirectional Conversion between Blocks and Text for App Inventor</a></h3>

**Ruanqianqian Huang** and Franklyn Turbak. In _2019 IEEE Blocks and Beyond Workshop (B&B)_, Memphis, TN, USA, 2019, pp. 87-89, doi: [10.1109/BB48857.2019.8941197.](10.1109/BB48857.2019.8941197.)

<!-- This extended abstract, presented in IEEE Blocks and Beyond Workshop, 2019, introduces a preliminary design for Venbrace based on a collection of design principles. -->

<!-- R. Huang and F. Turbak, "A Design for Bidirectional Conversion between Blocks and Text for App Inventor," 2019 IEEE Blocks and Beyond Workshop (B&B), Memphis, TN, USA, 2019, pp. 87-89, doi: [10.1109/BB48857.2019.8941197.](10.1109/BB48857.2019.8941197.) -->

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
  {% include base_path %}

  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}


