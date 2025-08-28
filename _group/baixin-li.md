---
layout: page               # keeps individual profile pages styled like the site
title: "Baixin Li"
role: "RA"
degrees:                     # NEW: ordered list (top = most recent)
  - degree: "M.S."
    field: "CS"
    university: "University of Hong Kong"
    year: 2025
  - degree: "B.S."
    field: "SE"
    university: "Dalian University of Technology"
    year: 2024
email: "u3638253@connect.hku.hk"
website: 
scholar:    # any of these social links are optional
github: “https://github.com/PunkyKnife”
twitter: 
linkedin: 
image: "/assets/img/people/baixin.jpg"      # put images here (create folder)
interests:
  - Machine Learning
  - LLM Watermarking
  - Data Science
order: 2                                     # for manual sorting within a role
alumni: false                                # set true and add `years:` if alumni
years:                                       # optional, for alumni listing
  start: 2025-08
  end: 
bio: >
  I am Baixin Li, and my current research interests include artificial intelligence and Large Language Model (LLM) watermark embedding. I obtained a Master's degree in Computer Science from the University of Hong Kong. Currently, I am focusing on developing efficient, lossless watermarking techniques for LLMs.
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
