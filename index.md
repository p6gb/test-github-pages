# markdown folder structure all files


{% assign doclist = site.pages | sort: 'url'  %}
{% assign filelist = site.static_files  %}
<ul>
    {% for file in filelist %}
        <li><a href="{{ site.baseurl }}{{ file.url }}">{{ doc.url }}</a></li>
    {% endfor %}

   {% for doc in doclist %}
        {% if doc.name contains '.md' or doc.name contains '.html' %}
               <li><a href="{{ site.baseurl }}{{ doc.url }}">{{ doc.url }}</a></li>
        {% endif %}
    {% endfor %}
</ul>