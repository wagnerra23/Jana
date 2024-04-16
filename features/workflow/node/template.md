# Template

Template lets you dynamically format and combine variables from previous nodes into a single text-based output using Jinja2, a powerful templating syntax for Python. It's useful for combining data from multiple sources into a specific structure required by subsequent nodes. The simple example below shows how to assemble an article by piecing together various previous outputs:

<figure><img src="../../../.gitbook/assets/output (1).png" alt="" width="375"><figcaption></figcaption></figure>

Beyond naive use cases, you can create more complex templates as per Jinja's [documentation](https://jinja.palletsprojects.com/en/3.1.x/templates/) for a variety of tasks. Here's one template that structures retrieved chunks and their relevant metadata from a knowledge retrieval node into a formatted markdown:

```Plain
{% raw %}
{% for item in chunks %}
### Chunk {{ loop.index }}. 
### Similarity: {{ item.metadata.score | default('N/A') }}

#### {{ item.title }}

##### Content
{{ item.content | replace('\n', '\n\n') }}

---
{% endfor %}
{% endraw %}
```

<figure><img src="../../../.gitbook/assets/output (2).png" alt=""><figcaption></figcaption></figure>

This template node can then be used within a Chatflow to return intermediate outputs to the end user, before a LLM response is initiated.

> The `Answer` node in a Chatflow is non-terminal. It can be inserted anywhere to output responses at multiple points within the flow.
