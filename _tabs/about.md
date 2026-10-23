---
# the default layout is 'page'
icon: fas fa-info-circle
order: 5
---
Hi there! I’m **John Paul Gonzales**, a second-year Bachelor of Science in Information Technology (BSIT) student at Batangas State University.

I have always been deeply attracted to technology because it provides people like me with a chronic illness a chance to experience the world, connect with others, and build meaningful things without physical limitations.

This website serves as a living record of my learning journey. It showcases my foundational skills, my growing knowledge in the IT field, and the various tech-related hobbies I am passionate about. I am currently focusing on building my skills from the ground up and embracing a beginner’s mindset to tackle new challenges.

## What I’m Learning & Using

My core focus right now spans a few key areas of technology:

- **Software Development:** Building enterprise logic and interactive experiences with Java.
- **Hardware & Embedded Systems:** Tinkering with IoT and robotics using microcontrollers like Arduino and ESP32.
- **Data Science & Analytics:** Exploring data structures and machine learning fundamentals using Python and SQL.

## Hobbies & Projects

Beyond the code, I love getting my hands dirty with the physical side of IT. Some of my favorite ongoing projects and hobbies include:

- **PC Building & Optimization:** Scouting cheap used PCs and parts on Shopee so I can finally experience having my own PC — a brand-new build that would last would need a minimum of ₱50k.

Feel free to look around my site to see my latest projects, notes, and the things I am currently building!

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
