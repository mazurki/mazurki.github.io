# Latest posts

<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {% if post.truncate %}
          {% assign trunc = post.truncate | plus: 0 %}
          {{ post.content | truncate: trunc }}
        {% else %}
          {{ post.content }}
        {% endif %}

      </div>

      <div class="date">
        <time datetime="{{ page.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date: "%b %-d, %Y" }}</time>
      </div>   

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>
