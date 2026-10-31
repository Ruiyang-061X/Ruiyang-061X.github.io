<!-- =====================================================================
     Publications
     Data lives in _data/publications.yml (newest entry first).
     ===================================================================== -->
<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for pub in site.data.publications.main %}

<li>
  <div class="title"><a href="{{ pub.pdf | default: pub.page }}">{{ pub.title }}</a></div>
  <div class="author">{{ pub.authors }}</div>
  <div class="periodical"><em>{{ pub.conference_short }}</em></div>
  <div class="links">
    {% if pub.pdf %}
    <a href="{{ pub.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Paper</a>
    {% endif %}
    {% if pub.code %}
    <a href="{{ pub.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
    {% endif %}
    {% if pub.page %}
    <a href="{{ pub.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
    {% endif %}
    <!-- BibTeX and the red status tag (e.g. "Oral") are intentionally
         disabled. To bring them back, add `bibtex:` / `notes:` fields
         to an entry in _data/publications.yml and uncomment below.
    {% if pub.bibtex %}
    <a href="{{ pub.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTeX</a>
    {% endif %}
    {% if pub.notes %}
    <strong><i style="color:#e74d3c">{{ pub.notes }}</i></strong>
    {% endif %}
    -->
  </div>
</li>
<br>

{% endfor %}

</ol>
</div>
