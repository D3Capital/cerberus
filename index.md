---
layout: default
title: Journal
---

<section class="time-intro">
  <p>Notes across time.</p>
</section>

<section class="time-axis">

  <div class="time-item time-past">
    <span class="time-label">What remains</span>
    <span class="time-word">Past</span>
    <span class="time-meaning">Memory · History · Experience</span>
  </div>

  <div class="time-item time-present">
    <span class="time-label">What is</span>
    <span class="time-word">Present</span>
    <span class="time-meaning">Observation · Decision · Life</span>
  </div>

  <div class="time-item time-future">
    <span class="time-label">What may come</span>
    <span class="time-word">Future</span>
    <span class="time-meaning">Possibility · Change · Becoming</span>
  </div>

</section>


<section class="journal">

  <div class="journal-heading">
    Journal
  </div>

  {% for post in site.posts %}

    <a class="journal-entry" href="{{ post.url | relative_url }}">

      <div class="entry-date">
        {{ post.date | date: "%d %b %Y" }}
      </div>

      <div class="entry-content">

        <h2 class="entry-title">
          {{ post.title }}
        </h2>

        <div class="entry-meta">
          {% if post.category %}
            {{ post.category }}
          {% else %}
            Notes
          {% endif %}
        </div>

      </div>

    </a>

  {% endfor %}

</section>
