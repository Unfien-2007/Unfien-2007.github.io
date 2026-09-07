---
icon: fas fa-diagram-project
order: 2
---

<!-- Each project is a normal Markdown file in the `_projects/` folder. -->

<div id="projects" class="row g-4">
  {% assign projects = site.projects | sort: 'date' | reverse %}
  {% for project in projects %}
    <div class="col-12 col-md-6">
      <article class="card h-100">
        {% if project.image %}
          {% assign src = project.image.path | default: project.image %}
          <a href="{{ project.url | relative_url }}">
            <img src="{{ src }}" class="card-img-top" alt="{{ project.image.alt | default: project.title }}">
          </a>
        {% endif %}
        <div class="card-body d-flex flex-column">
          <h2 class="card-title h5">
            <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
          </h2>
          {% if project.description %}
            <p class="card-text text-muted">{{ project.description }}</p>
          {% endif %}
          <div class="mt-auto pt-2 d-flex flex-wrap gap-1 align-items-center">
            {% if project.status %}
              <span class="badge bg-primary">{{ project.status }}</span>
            {% endif %}
            {% if project.tech %}
              {% for item in project.tech %}
                <span class="badge bg-secondary">{{ item }}</span>
              {% endfor %}
            {% endif %}
          </div>
          {% if project.date %}
            <small class="text-muted mt-2">
              <i class="far fa-calendar fa-fw me-1"></i>{{ project.date | date: '%b %e, %Y' }}
            </small>
          {% endif %}
        </div>
      </article>
    </div>
  {% else %}
    <p class="text-muted">
      No projects yet. Add a normal Markdown file in <code>_projects/</code> — e.g.
      <code>_projects/my-first-build.md</code> — and it will show up here automatically.
    </p>
  {% endfor %}
</div>
