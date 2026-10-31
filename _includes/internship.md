<!-- =====================================================================
     Internship
     Data lives in _data/internships.yml (newest entry first).
     Styled the same way as the Publications section above.
     ===================================================================== -->
<h2 id="internship" style="margin: 2px 0px -15px;">Internship</h2>

<div class="publications">
<ol class="bibliography">

{% for job in site.data.internships.main %}

<li>
  <div class="title">{{ job.role }}</div>
  <div class="author">{{ job.location }}</div>
  <div class="periodical"><em>{{ job.period }}</em></div>
  <p>{{ job.description }}</p>
  {% if job.project %}
  <div class="links">
    {% if job.project_link %}
    <a href="{{ job.project_link }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project: {{ job.project }}</a>
    {% else %}
    <strong>Project:</strong> {{ job.project }}
    {% endif %}
  </div>
  {% endif %}
</li>
<br>

{% endfor %}

</ol>
</div>
