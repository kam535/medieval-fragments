---
layout: page
title: Deep Search
permalink: /deep-search/
---
<script src="{{site.baseurl}}/assets/javascript/custom-search.js"></script>
<link rel="stylesheet" type="text/css" href="{{site.baseurl}}/assets/custom-search.css">
<div id="spinner"><i class="fa fa-spinner fa-spin"></i></div>
  
{% assign pids = site.medievalfragments | map: "pid" | compact %}
{% assign pids = pids | join: ','  | split: ','  | uniq | sort %}

{% assign labels = site.medievalfragments | map: "label" | compact %}
{% assign labels = labels | join: ','  | split: ','  | uniq | sort %}
 
<form role="search">
<div class="search-control" style="display:none;">
    <input type="search" id="object-search" name="query"
           placeholder="Keyword Search"
           aria-label="Search objects using keyword">
    <select id="pidselect" name="pid"
      aria-label="Dropdown for pid">
        <option value="">All pids</option>
        {% for pids in pids %}
          {% if pid != '' %}
          <option value="{{pid}}">{{pid}}</option>
          {% endif %}
        {% endfor %}
    </select>
    <select multiple="multiple" size="10" id="titleSelect" name="title"
      aria-label="label search">
      <optgroup label="Titles">
        {% for label in labels %}
          {% if label != '' %}
          <option value="{{label}}">{{label}}</option>
          {% endif %}
        {% endfor %}
      </optgroup>
    </select>
    <button class="custom_button" style="float: right;">Search</button>
</div>
</form>
<script>
window.addEventListener("load", function(){
    loadsearchtemplate();
    $('#spinner').hide();
});
</script>
