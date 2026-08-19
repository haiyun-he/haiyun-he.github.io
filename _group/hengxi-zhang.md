---
layout: page               # keeps individual profile pages styled like the site
title: "Hengxi Zhang"
role: "PhD Student"              # role: "PI" | "PhD Student" | "MPhil Student" | "RA"
degrees:                     # NEW: ordered list (top = most recent)
  - degree: "M.S."
    field: "Math"
    university: "Northwestern Polytechnical University"
    year: 2026
  - degree: "B.S."
    field: "Math"
    university: "Zhengzhou University"
    year: 2023
email: "hzhang955@connect.hkust-gz.edu.cn"
image: "/assets/img/people/hengxi.jpg"
# put images here (create folder)
interests:
  - LLM Watermarking
  - Mathematical Foundations of LLMs
  - Information Theory
order: 2                                     # for manual sorting within a role
alumni: false                                # set true and add `years:` if alumni
years:                                       # optional, for alumni listing
  start: 2026-08
  end: 
bio: >
  PhD student interested in the mathematics behind large language models. My current research focuses on LLM watermarking, and more broadly, I enjoy thinking about what mathematical ideas can tell us about these models. Outside research, I enjoy playing badminton and watching anime.
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