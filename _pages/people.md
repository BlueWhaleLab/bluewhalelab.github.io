---
layout: page
title: people
permalink: /people/
nav: true
nav_order: 1
description: The crew navigating the stars &amp; oceans of AI — meet the Blue Whale Lab.
_styles: |
  .post-header .post-title { display: none; }
  .post-header .post-description {
    font-size: 1.15rem;
    line-height: 1.6;
    color: var(--global-text-color-light);
    margin-bottom: 2.5rem;
  }
  .people-section { margin-bottom: 3rem; }
  .people-section-title {
    font-size: 1.4rem;
    margin-bottom: 1.25rem;
    padding-bottom: 0.4rem;
    border-bottom: 2px solid var(--global-divider-color);
    color: var(--global-text-color);
  }
  .people-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(190px, 1fr));
    gap: 1.5rem;
  }
  .member-card {
    background: var(--global-card-bg-color);
    border: 1px solid var(--global-divider-color);
    border-radius: 14px;
    padding: 1.5rem 1rem;
    text-align: center;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .member-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.12);
  }
  .member-avatar {
    width: 104px;
    height: 104px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 1rem;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  }
  .avatar-initials {
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, #2698ba 0%, #00369f 100%);
    color: #fff;
    font-size: 2rem;
    font-weight: 600;
    letter-spacing: 1px;
  }
  .member-name {
    font-size: 1.15rem;
    margin: 0 0 0.25rem;
    color: var(--global-text-color);
  }
  .member-name a {
    color: inherit;
    text-decoration: none;
    transition: color 0.2s ease;
  }
  .member-name a:hover { color: var(--global-theme-color); }
  .member-role {
    font-size: 0.85rem;
    color: var(--global-theme-color);
    margin: 0 0 0.75rem;
    font-weight: 500;
  }
  .member-bio {
    font-size: 0.85rem;
    color: var(--global-text-color-light);
    line-height: 1.5;
    margin: 0 0 0.9rem;
  }
  .member-bio-toggle {
    margin: 0 0 0.9rem;
    text-align: left;
  }
  .member-bio-toggle > summary {
    cursor: pointer;
    list-style: none;
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    font-size: 0.85rem;
    font-weight: 500;
    color: var(--global-theme-color);
    -webkit-user-select: none;
    user-select: none;
    transition: color 0.2s ease;
  }
  .member-bio-toggle > summary::-webkit-details-marker { display: none; }
  .member-bio-toggle > summary::after {
    content: "\25be";
    display: inline-block;
    font-size: 0.9rem;
    line-height: 1;
    transition: transform 0.2s ease;
  }
  .member-bio-toggle[open] > summary::after { transform: rotate(180deg); }
  .member-bio-toggle > summary:hover { color: var(--global-hover-color); }
  .member-bio-toggle .member-bio { margin: 0.6rem 0 0; }
  .member-links {
    display: flex;
    gap: 0.9rem;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: auto;
  }
  .member-links a {
    color: var(--global-text-color-light);
    font-size: 1.15rem;
    transition: color 0.2s ease;
  }
  .member-links a:hover { color: var(--global-theme-color); }
  .member-card.is-placeholder { border-style: dashed; }
  .member-card.is-placeholder .member-name {
    color: var(--global-text-color-light);
    font-weight: 500;
  }
  .member-card.is-placeholder .avatar-initials {
    background: linear-gradient(135deg, #9fb2bd 0%, #6c7a86 100%);
  }
  .member-card.featured {
    flex-direction: row;
    text-align: left;
    align-items: center;
    gap: 1.75rem;
    padding: 1.75rem;
  }
  .member-card.featured:hover {
    transform: none;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
  }
  .member-card.featured .member-avatar {
    width: 120px;
    height: 120px;
    margin-bottom: 0;
    flex-shrink: 0;
  }
  .member-card.featured .avatar-initials { font-size: 2.8rem; }
  .member-card.featured .member-info { flex: 1; }
  .member-card.featured .member-name { font-size: 1.25rem; }
  .member-card.featured .member-role { font-size: 0.95rem; }
  .member-card.featured .member-bio { font-size: 0.92rem; }
  .member-card.featured .member-links { justify-content: flex-start; }
  @media (max-width: 576px) {
    .member-card.featured {
      flex-direction: column;
      text-align: center;
    }
    .member-card.featured .member-links { justify-content: center; }
  }
---

{% for group in site.data.members.groups %}
<section class="people-section">
  <h2 class="people-section-title">{{ group.title }}</h2>

  {% if group.featured %}
    {% for member in group.members %}
    <div class="member-card featured{% if member.placeholder %} is-placeholder{% endif %}">
      {% if member.image %}
        <img class="member-avatar" src="{{ member.image | prepend: 'assets/img/' | relative_url }}" alt="{{ member.name }}">
      {% elsif member.placeholder %}
        <div class="member-avatar avatar-initials"><i class="fa-solid fa-user"></i></div>
      {% else %}
        {% assign parts = member.name | split: ' ' %}
        {% assign initials = '' %}
        {% for p in parts limit: 2 %}{% assign fl = p | slice: 0 %}{% assign initials = initials | append: fl %}{% endfor %}
        <div class="member-avatar avatar-initials">{{ initials | upcase }}</div>
      {% endif %}
      <div class="member-info">
        {% assign profile_url = member.links.website | default: member.links.scholar | default: member.links.github %}
        <h3 class="member-name">{% if profile_url %}<a href="{{ profile_url }}" target="_blank" rel="noopener">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}</h3>
        <p class="member-role">{{ member.role }}</p>
        {% if member.bio %}
        <details class="member-bio-toggle">
          <summary>Bio</summary>
          <p class="member-bio">{{ member.bio }}</p>
        </details>
        {% endif %}
        <div class="member-links">
          {% if member.links.website %}<a href="{{ member.links.website }}" title="Website"><i class="fa-solid fa-globe"></i></a>{% endif %}
          {% if member.links.email %}<a href="mailto:{{ member.links.email }}" title="Email"><i class="fa-solid fa-envelope"></i></a>{% endif %}
          {% if member.links.scholar %}<a href="{{ member.links.scholar }}" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
          {% if member.links.github %}<a href="{{ member.links.github }}" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
          {% if member.links.linkedin %}<a href="{{ member.links.linkedin }}" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>{% endif %}
          {% if member.links.twitter %}<a href="{{ member.links.twitter }}" title="X"><i class="fa-brands fa-x-twitter"></i></a>{% endif %}
          {% if member.links.orcid %}<a href="{{ member.links.orcid }}" title="ORCID"><i class="ai ai-orcid"></i></a>{% endif %}
          {% if member.links.cv %}<a href="{{ member.links.cv }}" title="CV"><i class="fa-solid fa-file-lines"></i></a>{% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  {% else %}
    <div class="people-grid">
      {% for member in group.members %}
      <div class="member-card{% if member.placeholder %} is-placeholder{% endif %}">
        {% if member.image %}
          <img class="member-avatar" src="{{ member.image | prepend: 'assets/img/' | relative_url }}" alt="{{ member.name }}">
        {% elsif member.placeholder %}
          <div class="member-avatar avatar-initials"><i class="fa-solid fa-user"></i></div>
        {% else %}
          {% assign parts = member.name | split: ' ' %}
          {% assign initials = '' %}
          {% for p in parts limit: 2 %}{% assign fl = p | slice: 0 %}{% assign initials = initials | append: fl %}{% endfor %}
          <div class="member-avatar avatar-initials">{{ initials | upcase }}</div>
        {% endif %}
        {% assign profile_url = member.links.website | default: member.links.scholar | default: member.links.github %}
        <h3 class="member-name">{% if profile_url %}<a href="{{ profile_url }}" target="_blank" rel="noopener">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}</h3>
        <p class="member-role">{{ member.role }}</p>
        {% if member.bio %}<p class="member-bio">{{ member.bio }}</p>{% endif %}
        <div class="member-links">
          {% if member.links.website %}<a href="{{ member.links.website }}" title="Website"><i class="fa-solid fa-globe"></i></a>{% endif %}
          {% if member.links.email %}<a href="mailto:{{ member.links.email }}" title="Email"><i class="fa-solid fa-envelope"></i></a>{% endif %}
          {% if member.links.scholar %}<a href="{{ member.links.scholar }}" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
          {% if member.links.github %}<a href="{{ member.links.github }}" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
          {% if member.links.linkedin %}<a href="{{ member.links.linkedin }}" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>{% endif %}
          {% if member.links.twitter %}<a href="{{ member.links.twitter }}" title="X"><i class="fa-brands fa-x-twitter"></i></a>{% endif %}
          {% if member.links.orcid %}<a href="{{ member.links.orcid }}" title="ORCID"><i class="ai ai-orcid"></i></a>{% endif %}
          {% if member.links.cv %}<a href="{{ member.links.cv }}" title="CV"><i class="fa-solid fa-file-lines"></i></a>{% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
  {% endif %}
</section>
{% endfor %}
