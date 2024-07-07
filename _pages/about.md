---
layout: about
title: about
permalink: /
subtitle: 

profile:
  align: right
  image: 
  image_circular: false # crops the image to make it circular
  more_info: >
    

news: false # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
latest_posts: false
social: false # includes social icons at the bottom of the page
---

{% assign start_date = site.exp_start_date | date: "%s" %}
{% assign current_date = "now" | date: "%s" %}
{% assign seconds_in_year = 60 | times: 60 | times: 24 | times: 365 %}
{% assign seconds_in_month = 60 | times: 60 | times: 24 | times: 30 %}

{% assign total_seconds = current_date | minus: start_date %}
{% assign years = total_seconds | divided_by: seconds_in_year %}
{% assign remaining_seconds = total_seconds | modulo: seconds_in_year %}
{% assign months = remaining_seconds | divided_by: seconds_in_month %}

Hello, I am a software engineer, passionate about `Data Structure and Algorithms, Operating Systems, Networking, Security, Operating systems, Data Storage and Data Backup`. Currently, I work as a __Software Engineer__ at *Dell Technologies*.

I have been working at Dell Technologies since *October 2020*, working on automation and development of Data Storage and Backup appliances, having a total of **{{ years }} years and {{ months }} months** of industrial experience.

[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/oapatil/)
&nbsp;&nbsp;
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/phileinsophos)
