## Variable

### Assign a Variable
```liquid
{% raw %}
{% assign my_string = "Hello World!" %}
{% assign my_int = 25 %}
{% assign my_float = 39.756 %}
{% assign foo = true %}
{% assign bar = false %}
{% endraw %}
```

### Output a Variable
```liquid
{% raw %}
{{ my_string }}
{% endraw %}
```