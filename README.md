# SYTWC_Practica_Jekyll

1. Run ```jekyll new *project_name*``` --> get defaut project structure

2. Check _config.yml

```
theme: minima
plugins:
  - jekyll-feed
```
3. Sass integration --> add the following to _config.yml

```
sass:
  style: compressed
```

4. Customize layout and style

+ add directories ```_includes```, ```_layouts```


+ Add *Menu* and *Logo* to header.html
![Jekyll](/images/custom.png)

+ Configure style in style.scss

```
header {
  padding: 20px;
  background-color: rebeccapurple;
  height: 70px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-wrap: wrap;
  img {  
  
    width: 20%;
    height: auto;
    
  }

    .main-nav ul {
	margin: 1em 0 .5em;
	text-align: center;
    }
    .main-nav li {
	display: inline;
    }
    .main-nav a {
    color: white;
	display: inline-block;
	padding: .5em 1.5em;
    }
}
```
**align-items: center** --> the flexbox items are aligned at the center of the cross axis.

+ Configure footer.html 

+ Add default layout for pages

```
<!DOCTYPE html>
<html>
  <head>
     {% include meta.html %} 
  </head>

  <body>
     {% include header.html %} 
    
    <div class="container">
      <div></div>
      <article>
         {{ content }} 
      </article>
      <div></div>
    </div>

     {% include footer.html %} 
  </body>

</html>
```
+ Customize styles for default --> class="container" in styles.scss

5. Fill out the home page --> Index.md 

+ Add image
+ Add tables structure

```
<div class="tables">
...
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
  ...
  </div>
  ````
+ Add styles for div, table

```
body {
  background-color: #ffffff !important;
  margin: 0px;
  padding: 0px;
  font-family: "Nunito", sans-serif;
  
  .tables {
    text-align: center;
    color: white;


  }
  .table {
   border: 1px solid gainsboro;
   float: left;
   width: 25%;
    
}
  .td-logo {
    background-image:  url({{site.url}}/assets/img/td-logo.jpg);
    height: 250px;
    width: 250px;
    vertical-align: bottom;
  }
}
```
**float: left** --> allows ordering multiple tables in one row (!)

6. App different categories of posts
![Jekyll](/images/posts.png)

7. Insert filters to the main content

```
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
...
</div>
```

## Result

```
 bundle exec jekyll serve
```
![Jekyll](/images/result_home.png)
![Jekyll](/images/result_post.png)