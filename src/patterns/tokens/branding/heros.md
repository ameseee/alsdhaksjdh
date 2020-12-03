---
title: Heros
maturity: planned
control: exclude
items: 
  - name: Main splash
    path: "https://d682ma8ami8n4.cloudfront.net/images/Turing_home2.jpg"
---
<style>
.set {
  display: flex;
  flex-wrap: wrap;
  margin: 0 -1rem;
  margin-top:  0;
  padding: 0;
  list-style: none;
}
li {
  flex: 1 0 20%;
  margin: 1rem;
}
.image {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  min-width: 280px;
  height: 300px;
  background-color: whitesmoke;
  border: 1px solid whitesmoke;
  margin-bottom: 1rem;
}
img {
  max-height: 100%;
}
p {
  margin: 0;
}
</style>
<ul class="set">
{% for item in page.items %} 
  <li>
    <div class="image"><img src="{{ item.path }}"/></div>
    <p class="header">{{ item.name }}</p>
    {% if item.path %}<a href="{{ item.path }}">{{ item.path }}</a>{% endif %}
  </li>
{% endfor %}
</ul>