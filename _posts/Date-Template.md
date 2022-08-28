---
published: False
layout: post
title: "Update"
date: 2022-08-28 012:54.0 -0700
categories: Template
author: James Alspach
---
Summary paragraph
{% capture string_with_newlines %}
important thoughts separated (as normal) with a single return

{% endcapture %}

{{ string_with_newlines | newline_to_br }}