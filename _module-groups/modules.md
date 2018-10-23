---
layout: page
title: ""
editbutton: false
---

{% assign sorted = site.project-modules | sort: 'title' %}
<h1>Modules</h1>
{% for module in sorted %}
  <div class="col-md-3 col-sm-4 col-xs-6" style="height: 225px;">
    <a href="{{site.baseurl}}{{module.url}}">
      <div>
      {% if module.thumbnail %}
      <img src="{{site.baseurl}}{{module.thumbnail}}" class="img-responsive" style="height: 150px; position: relative; left: 50%; top: 50%; margin-left: -75px;">
      {% else %}
      <img src="{{site.baseurl}}{{site.default-thumbnail}}" class="img-responsive" style="height: 150px; position: relative; left: 50%; top: 50%; margin-left: -75px;">
      {% endif %}
      </div>
      <div>
        <h4 style="text-align:center; vertical-align: bottom;">{{module.title}}</h4>
      </div>
    </a>
  </div>
{% endfor %}
