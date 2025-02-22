---
title: Collaborate With Us
layout: single
sidebar:
  nav: "contribute"
toc: true
toc_sticky: true
---

We warmly welcome your contribution to ROOT!

There are two ways in which you can contribute:



1. **Submit a pull request** <br>
   You can create a pull request on [GitHub](https://github.com/root-project/root){:target="_blank"}.
   Simply follow [our guidelines](https://github.com/root-project/root/blob/master/CONTRIBUTING.md).
   By providing code this way, you agree to transfer your copyright on the code to the "ROOT project".
   Of course you will be duly credited: for sizable contributions your name will appear in the
   [CREDITS](https://raw.githubusercontent.com/root-mirror/root/master/README/CREDITS){:target="_blank"}
   file shipped with every binary and source distribution.
   The copyright transfer helps us with effectively defending the project in case of litigation.

2. **Via the users' contribution section in the forum** <br>
   The Users' Forum has a [section](https://root-forum.cern.ch/c/my-root-app-and-ideas){:target="_blank"}
   which describes how to advertise your feature based on ROOT. It is the
   easiest way to make your code known to the community, even if it will not be
   automatically integrated in ROOT. Some contributions might
   become part of the repository - as it happened for RooFit, TMVA, Eve, to name a few.

Often it is useful to [contact us](https://root-forum.cern.ch){:target="_blank"} first to
discuss the code you want to develop or the bug you want to fix. You can do this directly
from your terminal, by typing: `root -b -e '.forum bug' -q`.

If you are an experienced contributor or are sure that you really found a bug, you can directly submit a
new issue on [GitHub](https://github.com/root-project/root/issues/new/choose) using the predefined
templates, or directly from your terminal:

```
root -b -e '.gh bug' -q
root -b -e '.gh feature' -q
root -b -e '.gh improvement' -q
``

## Picking up an idea

We maintain a set of "ideas" for talented scientists and developers to pick up.
An "idea" is a sketch of a development project, or a missing feature we would like to see in your ROOT!
You can inspect the ideas in the following list.

{% assign sorted = site.ideas | reverse %}

### Some Ideas <a href="{{ 'feed/ideas.xml' | relative_url }}"><img style="width:auto; height:1.0em;" src="{{'/assets/images/feed.svg' | relative_url}}"></a>

<ul>
{% for idea in sorted %}
{% if idea.state != "completed" %}
<li> {{idea.date | date_to_string }} <a href="{{ idea.url | relative_url }}"> {{ idea.title}} </a><br>
{{idea.summary}}
</li>
{% endif %}
{% endfor %}
</ul>

### Completed ideas

<ul>
{% for idea in sorted %}
{% if idea.state == "completed" %}
<li> {{idea.date | date_to_string }} <a href="{{ idea.url | relative_url }}"> {{ idea.title}} </a><br>
{{idea.summary}}
</li>
{% endif %}
{% endfor %}
</ul>
