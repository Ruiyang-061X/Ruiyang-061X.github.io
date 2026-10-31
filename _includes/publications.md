<!-- =====================================================================
     Publications
     Data lives in _data/publications.yml (newest entry first).
     Card layout follows the upstream minimal-light theme: a teaser
     image with the venue badge overlaid, next to the paper details.
     ===================================================================== -->
<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for pub in site.data.publications.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if pub.image %}
    <img src="{{ pub.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% if pub.conference_short %}
    <abbr class="badge">{{ pub.conference_short }}</abbr>
    {% endif %}
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
    <div class="title"><a href="{{ pub.page | default: pub.pdf }}">{{ pub.title }}</a></div>
    <div class="author">{{ pub.authors }}</div>
    <div class="periodical"><em>{{ pub.conference_short }}</em></div>
    <div class="links">
      {% if pub.pdf %}
      <a href="{{ pub.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Paper</a>
      {% endif %}
      {% if pub.page %}
      <a href="{{ pub.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
      {% endif %}
      {% if pub.code %}
      <a href="{{ pub.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if pub.blog %}
      <a href="{{ pub.blog }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Blog</a>
      {% endif %}
      <!-- BibTeX and the red status tag (e.g. "Oral") are intentionally
           disabled, and the abstract/introduction text is intentionally
           omitted. To bring them back, add `bibtex:` / `notes:` /
           `abstract:` fields to an entry in _data/publications.yml and
           uncomment below.
      {% if pub.bibtex %}
      <a href="{{ pub.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTeX</a>
      {% endif %}
      {% if pub.notes %}
      <strong><i style="color:#e74d3c">{{ pub.notes }}</i></strong>
      {% endif %}
      -->
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
