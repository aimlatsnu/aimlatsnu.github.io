---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

#layout: home
---


<section id="publications">
    <h2 class="mb-4">Publications</h2>
    {% assign sorted_publications = site.data.publications | sort: "year" | reverse %}
    <ul class="list-group">
        {% for pub in sorted_publications %}
        <li class="list-group-item">
            <strong>{{ pub.title }}</strong> - {{ pub.year }}<br>
            Authors: {{ pub.authors | join: ", " }}<br>
            {% if pub.journal %}Journal: {{ pub.journal }}{% endif %}
            {% if pub.conference %}Conference: {{ pub.conference }}{% endif %}
            <br><a href="{{ pub.link }}" target="_blank">Read more</a>
        </li>
        {% endfor %}
    </ul>
</section>