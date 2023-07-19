# Fielname:
  ```
{{author}} - {{title}}
```

# Page Title
```
  # {{ title }}
```
# Page Metadata:
```
{% if image_url -%}
![rw-book-cover]({{image_url}})

{% endif -%}
{% if url -%}
- URL: {{url}}
{% endif -%}
```

# Highlights Header
```
{% if is_new_page %}
## Highlights
{% elif has_new_highlights -%}
## New highlights added {{date|date('F j, Y')}} at {{time}}
{% endif -%}
```

# Highlight
```
### {% if highlight_location != "View Highlight" and highlight_location != "View Tweet" %}{{highlight_location}}{% else %}id{{highlight_id}}{% endif %}

> {{ highlight_text }}
{% if highlight_note %}
- [n] {{ highlight_note }}
{% endif %}
{% if highlight_location and highlight_location_url %} * [{{highlight_location}}]({{highlight_location_url}}){% elif highlight_location %} ({{highlight_location}}){% endif %}
```

# YAML frontmatter
```
Author: {{author}}
Tags: RW_inbox, readwise
Note Created: <% tp.date.now("dddd Do MMMM YYYY HH:mm") %>
Last modified: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm") %>
```
