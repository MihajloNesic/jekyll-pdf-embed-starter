---
layout: single
title:  "jekyll-pdf-embed test"
date:   2021-10-23 07:25:53 +0200
categories: jekyll plugin
pdf_file: "/jekyll-pdf-embed-starter/files/dummy.pdf"
---

{% highlight ruby %}
{% raw %}
{% pdf "https://mihajlonesic.gitlab.io/files/loremipsum.pdf" %}
{% endraw %}
{% endhighlight %}

{% pdf "https://mihajlonesic.gitlab.io/files/loremipsum.pdf" %}

---

Base URL must be present if `baseurl` is set in `_config.yml`.
In this example, `minimal-mistakes-pdf-example` is prepended to file location `/files/dummy.pdf`.


{% highlight ruby %}
{% raw %}
{% pdf "/jekyll-pdf-embed-starter/files/dummy.pdf" no_link height=300px %}
{% endraw %}
{% endhighlight %}

{% pdf "/jekyll-pdf-embed-starter/files/dummy.pdf" no_link height=300px %}

Another example is using file from front matter

{% highlight ruby %}
{% raw %}
---
pdf_file: "/jekyll-pdf-embed-starter/files/dummy.pdf"
---
{% pdf {{ page.pdf_file }} %}
{% endraw %}
{% endhighlight %}

{% pdf {{ page.pdf_file }} %}
