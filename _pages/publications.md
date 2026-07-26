---
layout: archive
title: "Publications"
permalink: /publications/
---

{% include base_path %}

{% assign pubs = site.publications | sort: "date" | reverse %}

{%- comment -%} Distinct years, newest first (delimiter-accumulator) {%- endcomment -%}
{%- assign year_order = "|" -%}
{%- for pub in pubs -%}
  {%- capture yk %}|{{ pub.year }}|{% endcapture -%}
  {%- unless year_order contains yk %}{% assign year_order = year_order | append: pub.year | append: "|" %}{% endunless -%}
{%- endfor -%}
{%- assign years = year_order | split: "|" -%}

<div class="pub-layout">
  <nav class="pub-years" aria-label="Jump to year">
    {% for y in years %}{% if y != "" %}<a href="#y{{ y }}" data-year="{{ y }}">{{ y }}</a>{% endif %}{% endfor %}
  </nav>

  <div class="pub-main">
    {% assign has_equal = pubs | where: "equal_contrib", true %}
    {% if has_equal.size > 0 %}<p class="pub-note">* Equal contribution</p>{% endif %}
    <ul class="pub-list">
      {% assign last_year = "" %}
      {% for pub in pubs %}
        {% if pub.year != last_year %}{% assign ys = true %}{% assign last_year = pub.year %}{% else %}{% assign ys = false %}{% endif %}
        {% include pub-entry.html pub=pub year_start=ys %}
      {% endfor %}
    </ul>
  </div>
</div>

<script>
  (function () {
    var rail = document.querySelector('.pub-years');
    if (!rail) return;
    var links = Array.prototype.slice.call(rail.querySelectorAll('a'));
    var anchors = links.map(function (a) { return document.getElementById('y' + a.dataset.year); });
    var OFFSET = 90;
    function setActive(i) {
      links.forEach(function (a, idx) { a.classList.toggle('is-active', idx === i); });
    }
    function onScroll() {
      var active = 0;
      anchors.forEach(function (el, i) {
        if (el && el.getBoundingClientRect().top - OFFSET <= 0) active = i;
      });
      // Near the page bottom the last (short) years can't reach the top — pin the final year.
      if (window.innerHeight + window.scrollY >= document.documentElement.scrollHeight - 2) {
        active = anchors.length - 1;
      }
      setActive(active);
    }
    var ticking = false;
    function schedule() {
      if (ticking) return;
      ticking = true;
      requestAnimationFrame(function () { onScroll(); ticking = false; });
    }
    links.forEach(function (a, i) {
      a.addEventListener('click', function () { setActive(i); });
    });
    window.addEventListener('scroll', schedule, { passive: true });
    window.addEventListener('resize', schedule);
    onScroll();
  })();
</script>
