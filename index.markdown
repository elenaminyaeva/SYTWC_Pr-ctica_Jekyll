---
layout: default
---

<h3>Welcome to my Blog</h3>

<div>
 <img src="{{site.url}}/assets/img/Logo_ULL.jpg" alt="Universidad de la Laguna">
</div>

<div class="tables">
  {% for post in site.categories.jekyll %}
  <table class="table">
  <tr>
  <td class="td-logo">Principal</td>
  </tr>
  <tr>
  <td>I am a very simple card.
  I am good at containing small bits of information.</td>
  </tr>
  <tr>
    <td><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></td>
  </tr>
    </table>
  {% endfor %}

  {% for post in site.categories.norte %}
  <table class="table">
  <tr>
  <td class="td-logo">Zona Norte</td>
  </tr>
  <tr>
  <td>I am a very simple card.
  I am good at containing small bits of information.</td>
  </tr>
  <tr>
    <td><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></td>
  </tr>
    </table>
 {% endfor %}

{% for post in site.categories.south %}
 <table class="table">
  <tr>
  <td class="td-logo">Zona Sur</td>
  </tr>
  <tr>
  <td>I am a very simple card.
  I am good at containing small bits of information.</td>
  </tr>
  <tr>
    <td><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></td>
  </tr>
    </table>
 {% endfor %}

{% for post in site.categories.x %}
  <table class="table">
  <tr>
  <td class="td-logo">Zona X</td>
  </tr>
  <tr>
  <td>I am a very simple card.
  I am good at containing small bits of information.</td>
  </tr>
  <tr>
    <td><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></td>
  </tr>
    </table>
 {% endfor %}
 
</div>