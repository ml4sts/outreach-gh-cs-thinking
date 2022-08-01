# Customize your Site Further



## Add a Blog


````
## News

See the [news page](news.md) for a more complete list.

```{postlist}
:date: "%Y-%m-%d"
:format: "{date} : {title}"
:excerpts:
```
````

## Add pannels

These pages use [sphinx panels]().  Add yourself at the top of the relevant section.

```

:column: col-4

NAME

^^^

Role and optional bio
+++

{link-badge}`https://github.com/gh-username,"GitHub",cls=badge-dark text-white`

---

```

Formatting notes:
- The `^^^` separates your name/title from the body
- `+++` separates the links from the body
- `---` spearates people/projects

For the link badges, look at others on the page to see style conventions.  
```
{link-badge}`http://url/to/site/,"text to display",cls=style-info`
```

## Allow Commenting

add this to `_templates/layout.html`

You will need to use the GitHub Graph API to get the two `-id` variable
values.  

See Giscus for more.


````
{%- extends "pydata_sphinx_theme/layout.html" %}

{% block docs_body %}
{{ super() }}
<!-- Add a comment box underneath the page's content -->
<!-- <script src="https://giscus.app/client.js"
        data-repo="username/username.github.io"
        data-repo-id=""
        data-category="Blog comments"
        data-category-id=""
        data-mapping="pathname"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-theme="light"
        data-lang="en"
        crossorigin="anonymous"
        async>
</script> -->
{% endblock %}

````
