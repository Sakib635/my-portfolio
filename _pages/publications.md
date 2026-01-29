---
title: "Publications"
permalink: /publications/
layout: default
---

## Publications

{% for pub in site.data.publications %}
- **{{ pub.title }}**  
  {{ pub.authors }}  
  *{{ pub.journal }}*  
  [Link]({{ pub.link }})
{% endfor %}
