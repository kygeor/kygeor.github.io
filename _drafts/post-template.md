---
layout: post
title: post title
date: 2026-01-01 10:00:00+0200
description: one-line summary shown in the list of writings
tags: [scientific-ml, numerical-analysis]
categories: []
giscus_comments: false
related_posts: false
toc:
  sidebar: left
# To cite papers from _bibliography/papers.bib in the text, set
# citation: true
# and write {% cite georgiou2025fredholm %}
---

Drafts in `_drafts/` are not published. To publish, move the file to `_posts/` and rename it `YYYY-MM-DD-slug.md`.

## Mathematics

Inline math uses `$$ ... $$` inside a sentence, e.g. $$ \|K\|_{L^2} < 1 $$. Display math:

$$
\begin{equation}
\label{eq:fredholm}
f(x) = g(x) + \int_{\Omega} K(x, z)\, f(z)\, dz .
\end{equation}
$$

Equation \eqref{eq:fredholm} can be referenced like this.

## Code

```python
import numpy as np

def picard(K, g, n_iter=50):
    f = g.copy()
    for _ in range(n_iter):
        f = g + K @ f
    return f
```

## Figures

Put images in `assets/img/` and include them with

{% raw %}

```liquid
{% include figure.liquid loading="eager" path="assets/img/your-figure.png" class="img-fluid rounded z-depth-1" zoomable=true %}
```

{% endraw %}

## Jupyter notebooks

Put the notebook in `assets/jupyter/` and include it with

{% raw %}

```liquid
{::nomarkdown}
{% assign jupyter_path = 'assets/jupyter/your-notebook.ipynb' | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/your-notebook.ipynb %}{% endcapture %}
{% if notebook_exists == 'true' %}
  {% jupyter_notebook jupyter_path %}
{% endif %}
{:/nomarkdown}
```

{% endraw %}
