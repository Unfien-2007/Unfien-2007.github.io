---
icon: fas fa-user
order: 1
---

I'm **John Paul Gonzales**, a second-year BSIT student at Batangas State University in
the Philippines. I like taking projects from `git push` to a live, running service — and
documenting what breaks along the way.

I got into IT because it gives someone with a chronic illness a way to build and take
part without physical limits. This site is where I keep the record: projects, notes, and
whatever I'm learning next.

**Open to internships and OJT opportunities.**

[Unfienproductions@gmail.com](mailto:Unfienproductions@gmail.com) · [GitHub](https://github.com/Unfien-2007) · [LinkedIn](https://www.linkedin.com/in/john-paul-gonzales-a9b199389) · [RSS](/feed.xml)

## Education

**Bachelor of Science in Information Technology (BSIT)**\
Batangas State University · 2nd year

Member, **Junior Philippine Computer Society (JPCS)** — Malvar Chapter

## What I'm focused on

- **Deployment & operations** — getting projects live and keeping them running:
  GitHub Actions, GitHub Pages, CI/CD, PWA caching
- **Python for data** — learning data analysis (pandas) through coursework and DataCamp
- **Embedded & hardware** — simple ESP32/Arduino experiments and a budget desktop build

## Tech Stack

**Used in coursework & projects** — Java · Python · SQL · SQLite · Git · GitHub ·
GitHub Actions · Arduino · ESP32

**Currently learning** — Linux administration · Vercel · Python data analysis (pandas)

**Curious about** — Docker · self-hosting · homelabs

## Featured Projects

- **[This site](/)** — Jekyll + Chirpy, deployed and maintained with GitHub Actions,
  with PWA caching and analytics
- **[Dell Vostro 3671 Build](/projects/dell-vostro-3671/)** — build log for my first
  desktop, upgraded one part at a time

More on the [Projects page](/projects/).

## Hobbies & Projects

Beyond the code, I like getting my hands dirty with the physical side of IT:

- **PC Building & Optimization:** Scouting cheap used PCs and parts on Shopee so I can
  finally experience having my own PC — a brand-new build that would last would need a
  minimum of ₱50k.

---

## Personal Writing

Not everything here is technical. These pieces are more personal — journal entries and
opinions — so I keep them off the home page and out of search engine results. They're
still public and browsable if you'd like to read them.

{% assign personal_posts = site.posts | where: 'hidden', true %}
{% if personal_posts.size > 0 %}
<ul>
  {% for post in personal_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="text-muted">— {{ post.date | date: "%b %-d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
{% else %}
<p class="text-muted">Nothing published yet.</p>
{% endif %}
