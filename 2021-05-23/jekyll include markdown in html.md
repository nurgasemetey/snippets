### jekyll include markdown in html


[Include markdown file in html file - Stack Overflow](https://stackoverflow.com/questions/48994088/include-markdown-file-in-html-file "Include markdown file in html file - Stack Overflow")


 

```
{% capture p1 %}{% include projects.md %}{% endcapture %}
{{ p1 | markdownify }}


create projects.md in _includes
```
