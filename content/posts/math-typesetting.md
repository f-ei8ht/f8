---
author: Hugo Authors
title: HI there
date: 2021-02-25
description: A brief guide to setup KaTeX
categories:
  - syntax
math: true
---

Mathematical notation in a Hugo project can be enabled by using third party JavaScript libraries.
<!--more-->

In this example we will be using [KaTeX](https://katex.org/)

- Create a partial under `/layouts/partials/math.html`
- Within this partial reference the [Auto-render Extension](https://katex.org/docs/autorender.html) or host these scripts locally.
- Include the partial in your templates like so:  

```bash
{{ if or .Params.math .Site.Params.math }}
{{ partial "math.html" . }}
{{ end }}
```

- To enable KaTex globally set the parameter `math` to `true` in a project's configuration
- To enable KaTex on a per page basis include the parameter `math: true` in content files
- Saif Ali Khan

**Note:** Use the online reference of [Supported TeX Functions](https://katex.org/docs/supported.html)


### Examples



Block math:
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$

$$
\left(\LARGE{AB}\right)
$$

\\(\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…\\)


$$
\begin{alignat}{2}
   10&x+&3&y=2\\\\
   3&x+&13&y=4
\end{alignat}
$$