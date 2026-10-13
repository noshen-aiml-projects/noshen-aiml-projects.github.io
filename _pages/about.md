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

I'm an AI/ML engineer and a Master of Information & Data Science (MIDS) student at UC Berkeley. I work across the model lifecycle — framing the problem, building data pipelines, fine-tuning and evaluating models, and keeping them healthy once they're deployed.

Currently I'm an **AI/ML Engineering Intern and Research Lead at Bytespace**, where I lead a research team running systematic ML experiments and build task-specific models with supervised fine-tuning, LoRA, quantization, and distillation, backed by custom evaluation frameworks. Before that, I was a Machine Learning Engineer with **WiCDS**, building an equity-aware scoring model for the Hayward Parks Department.

Before grad school I spent three years at **IBM** as a software engineer, automating deployments across client production environments with Ansible, Terraform, and Jenkins, and leading security-analytics work that resolved 60+ compliance issues. I did my B.Sc. in Computer Science at Ontario Tech University, where my honors thesis applied ML to anomaly detection on automotive CAN bus data.

**Interests:** LLMs and NLP, fine-tuning and model compression, evaluation and model reliability, fairness, and agentic workflows.

Take a look at my [projects](#projects) below, my [resume](/cv/), and my [articles](/blog/) — or reach out by email.

<div style="clear: both"></div>

<h2
  id="projects"
  style="margin-top: 3.5rem; padding-top: 2rem; border-top: 1px solid var(--global-divider-color); color: var(--global-theme-color); font-weight: 500"
>
  projects
</h2>

<div class="projects">
  <div class="row row-cols-1 row-cols-md-3">
    {% assign sorted_projects = site.projects | sort: "importance" %}
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>
