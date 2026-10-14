---
layout: about
title: about
permalink: /
subtitle: AI/ML Engineer · Master of Information & Data Science, <a href='https://www.ischool.berkeley.edu/'>UC Berkeley</a>

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular

selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items

latest_posts:
  enabled: false # turn on once you publish your first article
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I am an AI/ML engineer completing my Master of Information and Data Science at UC Berkeley. I also hold a B.Sc. in Computer Science from Ontario Tech University.

Right now I am an AI/ML researcher at Bytespace, a startup building AI tooling. Day to day, I design experiments, fine-tune models and make them smaller and faster, and build evaluation frameworks that show whether a model actually works. One of my favorite projects is an NLP pipeline that searches more than a million Hugging Face models to find the best fit for a given use case.

The work I care about most is using AI on problems both big and small. One day that might mean helping a cancer clinic figure out where AI fits into pathology and genomics. Another day it might mean helping a small business automate its outreach. Whatever the project, I look for the cleanest, simplest and most robust way to solve problems worth solving. My technical interests are fine-tuning and model efficiency, rigorous evaluation, NLP, and agentic systems that reliably get real work done.

Building a good model is only half the job. Before Bytespace, I spent three years at IBM in DevOps and automation, and that taught me how to deploy, scale and maintain systems cleanly, so what I build keeps working long after launch.

At Berkeley, I am part of WiCDS (Women in Computing and Data Science). There I work alongside talented women in tech on projects with real community impact, like helping the City of Hayward prioritize park maintenance more fairly.

Through all of it, teaching has been my constant. I started out tutoring neighbors and classmates. Later I was a teaching assistant at Ontario Tech and taught at reputable academies like Mathnasium and Hippocampus. Teaching is how I share my love of tech, and it keeps me learning, because explaining something well forces me to understand it deeply.

If you’re working on a problem worth solving, want to collaborate on AI research, or just want to talk about teaching and tech, I’d love to hear from you.

Reach out at [noshen@berkeley.edu](mailto:noshen@berkeley.edu) or connect with me on [LinkedIn](https://www.linkedin.com/in/noshen-habib).

<div style="clear: both"></div>

<h2
  id="projects"
  style="margin-top: 3.5rem; padding-top: 2rem; border-top: 1px solid var(--global-divider-color); color: var(--global-theme-color); font-weight: 500"
>
  Projects
</h2>

<div class="projects">
  <div class="row row-cols-1 row-cols-md-3">
    {% assign sorted_projects = site.projects | sort: "importance" %}
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>
