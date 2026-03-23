---
layout: default
title: Provisional schedule
description: Provisional schedule of the class
nav_order: 3
---

# Provisional schedule

The first bloc takes place at the MUC.DAI and the second and third at the Wavelab, see [Directions and useful infos]({% link content/directions.md %}).

{% for schedule in site.schedules %}
{{ schedule }}
{% endfor %}
