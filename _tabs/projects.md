---
icon: fas fa-diagram-project
order: 2
---

<!-- Each project is a normal Markdown file in the `_projects/` folder. -->

{% include lang.html %}

<div id="post-list" class="flex-grow-1 px-xl-1">
  {% assign projects = site.projects | sort: 'date' | reverse %}
  {% for project in projects %}
    <article class="card-wrapper card">
      <a href="{{ project.url | relative_url }}" class="post-preview row g-0 flex-md-row-reverse">
        {% assign card_body_col = '12' %}

        {% if project.image %}
          {% assign src = project.image.path | default: project.image %}
          {% assign alt = project.image.alt | xml_escape | default: project.title %}
          <div class="col-md-5">
            <img src="{{ src }}" alt="{{ alt }}">
          </div>
          {% assign card_body_col = '7' %}
        {% endif %}

        <div class="col-md-{{ card_body_col }}">
          <div class="card-body d-flex flex-column">
            <h1 class="card-title my-2 mt-md-0">{{ project.title }}</h1>

            <div class="card-text content mt-0 mb-3">
              <p>{{ project.description | default: project.excerpt | strip_html | truncate: 200 }}</p>
            </div>

            <div class="post-meta flex-grow-1 d-flex align-items-end">
              <div class="me-auto">
                {% if project.date %}
                  <!-- posted date -->
                  <i class="far fa-calendar fa-fw me-1"></i>
                  {% include datetime.html date=project.date lang=lang %}
                {% endif %}

                {% if project.status %}
                  <i class="fas fa-circle-info fa-fw ms-2 me-1"></i>
                  <span>{{ project.status }}</span>
                {% endif %}

                {% if project.tech and project.tech.size > 0 %}
                  <i class="fas fa-code fa-fw ms-2 me-1"></i>
                  <span>{{ project.tech | join: ', ' }}</span>
                {% endif %}
              </div>

              {% if project.pin %}
                <div class="pin ms-1">
                  <i class="fas fa-thumbtack fa-fw"></i>
                  <span>{{ site.data.locales[lang].post.pin_prompt }}</span>
                </div>
              {% endif %}
            </div>
            <!-- .post-meta -->
          </div>
          <!-- .card-body -->
        </div>
      </a>
    </article>
  {% else %}
    <p class="text-muted">
      No projects yet. Add a normal Markdown file in <code>_projects/</code> — e.g.
      <code>_projects/my-first-build.md</code> — and it will show up here automatically.
    </p>
  {% endfor %}
</div>
<!-- #post-list -->
