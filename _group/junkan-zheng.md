---
layout: page               # keeps individual profile pages styled like the site
title: "Junkan Zheng"
role: "RA"
degrees:                     # NEW: ordered list (top = most recent)
  - degree: "M.S."
    field: "Math"
    university: "Renmin University of China"
    year: 2027 Expected
  - degree: "B.S."
    field: "Econ"
    university: "Zhejiang University"
    year: 2024
email: "2024104166@ruc.edu.cn"
website: 
scholar:    # any of these social links are optional
github: 
twitter: 
linkedin: 
image: "/assets/img/people/Junkan.jpg"      # put images here (create folder)
interests:
  - Information-Theoretic Analysis of Generalization Error in Learning Systems
  - Optimal Transport and Applications in Data Science
  - Mathematical Foundations of Complex Systems
order: 3                                     # for manual sorting within a role
alumni: false                                # set true and add `years:` if alumni
years:                                       # optional, for alumni listing
  start: 2025-08
  end: 
bio: >
  Junkan Zheng is a graduate student at the School of Mathematics, Renmin University of China.  
  In Fall 2025, he will be a research assistant in Prof. Haiyun’s group at HKUST (GZ).  
  His research focuses on building mathematical foundations for learning systems. He is particularly interested in using information-theoretic tools to analyze generalization error in learning systems, and in applying optimal transport theory to solve problems in data science.  
  These interests are motivated by a broader perspective in complex systems science. Current mathematical tools offer limited explanatory and guiding power for complex systems: suitable tools may not yet exist, or existing theories may not have been properly developed or applied. He aims to advance these directions to gain deeper insights into their behavior.
---

<div class="row g-4 align-items-start">
  <div class="col-12 col-md-4">
    {% if page.image %}
      <img src="{{ page.image | relative_url }}" alt="{{ page.title }}" class="img-fluid rounded shadow-sm mb-3">
    {% endif %}
    <div class="small">
      {% if page.email %}<div><i class="fas fa-paper-plane"></i> <a href="mailto:{{ page.email }}">{{ page.email }}</a></div>{% endif %}
      {% if page.website %}<div><i class="fa-solid fa-globe"></i> <a href="{{ page.website }}">{{ page.website }}</a></div>{% endif %}
      {% if page.scholar %}<div><i class="ai ai-google-scholar"></i> <a href="{{ page.scholar }}">Google Scholar</a></div>{% endif %}
      {% if page.github %}<div><i class="fa-brands fa-github"></i> <a href="https://github.com/{{ page.github }}">{{ page.github }}</a></div>{% endif %}
      {% if page.twitter %}<div><i class="fa-brands fa-x-twitter"></i> <a href="https://twitter.com/{{ page.twitter }}">{{ page.twitter }}</a></div>{% endif %}
      {% if page.linkedin %}<div><i class="fa-brands fa-linkedin"></i> <a href="{{ page.linkedin }}">LinkedIn</a></div>{% endif %}
      {% if page.years.start or page.years.end %}
        <div class="mt-2"><span class="fw-semibold">Years:</span>
          {% if page.years.start %}{{ page.years.start }}{% endif %} – {% if page.years.end %}{{ page.years.end }}{% else %}present{% endif %}
          {% if page.alumni == true %}<span class="badge bg-outline-primary ms-2">Alumni</span>{% endif %}
        </div>
      {% endif %}
    </div>
  </div>

  <div class="col-12 col-md-8">
    {% if page.degrees %}
      <h3 class="h5">Degrees</h3>
      <ul class="mb-3">
        {% for d in page.degrees %}
          <li>{{ d.degree }} in {{ d.field }}, {{ d.university }}{% if d.year %} ({{ d.year }}){% endif %}</li>
        {% endfor %}
      </ul>
    {% endif %}

    {% if page.interests %}
      <h3 class="h5">Research Interests</h3>
      <p>{{ page.interests | join: ", " }}</p>
    {% endif %}

    {% if page.bio %}
        <h3 class="h5">Bio</h3>
        <div class="mt-3">{{ page.bio | markdownify }}</div>
    {% endif %}
  </div>
</div>
