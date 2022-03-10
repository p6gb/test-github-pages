# markdown folder structure include jpgs 2


{% assign doclist = site.pages | sort: 'url'  %}
<ul>
   {% for doc in doclist %}
               <li><a href="{{ site.baseurl }}{{ doc.url }}">{{ doc.url }}</a></li>

        {% if doc.name contains '.md' or doc.name contains '.html' or doc.name contains '.jpg' %}
        {% endif %}
    {% endfor %}
</ul>