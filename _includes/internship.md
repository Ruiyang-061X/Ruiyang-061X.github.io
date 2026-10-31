<!-- =====================================================================
     Internship
     Data lives in _data/internships.yml (newest entry first).
     Card layout mirrors Publications (image column + details column),
     but the image is a plain company logo with no badge, and the
     project is plain text rather than a button.
     ===================================================================== -->
<h2 id="internship" style="margin: 2px 0px -15px;">Internship</h2>

<div class="publications">
<ol class="bibliography">

{% for job in site.data.internships.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if job.image %}
    <img src="{{ job.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
    <strong>{{ job.role }}</strong>
    <br>
    {{ job.period }}
    <br>
    <em>{{ job.city }}</em>, {{ job.country }}
    <br>
    <strong>Topics:</strong> {{ job.topics }}
    {% if job.project %}
    <br>
    <strong>Project:</strong> {% if job.project_link %}<a href="{{ job.project_link }}">{{ job.project }}</a>{% else %}{{ job.project }}{% endif %}
    {% endif %}
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
