---
header: images/background.jpg
header-dark: true
nav_links:
  - name: Home
    link: /
  - name: Research
    link: /research
  - name: Projects
    link: /projects
  - name: Team
    link: /team
  - name: Contact
    link: /contact
---

# Artificial Intelligence & Robotics Center

**Pioneering the Future of Technology**

The AIR Center at VIT-AP University is at the forefront of innovation, exploring cutting-edge technologies in AI, deep learning, and robotics to solve tomorrow's challenges.

{%
include button.html
link="research"
text="Explore Our Work"
icon="fa-solid fa-rocket"
%}

{% include section.html %}

## Innovation Hub

The AIR Lab is an initiative brought to reality at VIT-AP University and is the first of its kind in the country. Set up with the aim of exploring the latest technologies in the field, such as deep learning, machine learning, and robotics, the AIR Lab has given students a platform to not only learn about these technologies but also work with them to build something unique. The lab fosters an ideal technology-rich environment that promotes student-driven learning, offering a new and innovative approach compared to traditional methods. The lab has grown with more students bringing in unique and valuable ideas. With the support of faculty, it aims to be a hub where cutting-edge technologies and innovative ideas can flourish and be brought to life.

{% include section.html %}

## Latest News

{:.center}

<div class="news-container" style="max-width: 100%; margin: 30px auto; position: relative;">
  <div class="news-column" style="width: 100%;">
    {% for post in site.posts limit:5 %}
      <div class="news-item" style="margin-bottom: 15px; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
        <div style="display: flex; align-items: center;">
          {% if post.image %}
          <div style="width: 100px; height: 80px; flex-shrink: 0; overflow: hidden;">
            <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" style="width: 100%; height: 100%; object-fit: cover;">
          </div>
          {% else %}
          <div style="width: 100px; height: 80px; background-color: #f0f0f0; display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
            <i class="fa-regular fa-newspaper" style="font-size: 24px; color: #888;"></i>
          </div>
          {% endif %}

          <div style="padding: 10px; flex-grow: 1;">
            <p style="color: #666; margin: 0 0 4px 0; font-size: 0.8em;">{{ post.date | date: "%b %d, %Y" }}</p>
            <h3 style="margin: 0 0 4px 0; font-size: 1em; line-height: 1.2; overflow: hidden; text-overflow: ellipsis; display: -webkit-box; -webkit-line-clamp: 1; -webkit-box-orient: vertical;">
              <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: inherit;">{{ post.title }}</a>
            </h3>
            <p style="margin: 0; font-size: 0.85em; color: #555; overflow: hidden; text-overflow: ellipsis; display: -webkit-box; -webkit-line-clamp: 1; -webkit-box-orient: vertical;">
              {{ post.excerpt | strip_html | truncate: 80 }}
            </p>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>

<div style="text-align: center; margin-top: 20px;">
{%
include button.html
link="blog"
text="View All News"
icon="fa-solid fa-newspaper"
%}
</div>

{% include section.html %}

## Key Statistics

{:.center}

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 30px; margin: 40px 0;">
  <div style="text-align: center; flex: 1; min-width: 120px; margin-bottom: 20px;">
    <div style="font-size: calc(2em + 1vw); font-weight: bold; color: var(--primary);">25+</div>
    <div style="font-size: 1.2em;">Research Publications</div>
  </div>
  <div style="text-align: center; flex: 1; min-width: 120px; margin-bottom: 20px;">
    <div style="font-size: calc(2em + 1vw); font-weight: bold; color: var(--primary);">15+</div>
    <div style="font-size: 1.2em;">Ongoing Projects</div>
  </div>
  <div style="text-align: center; flex: 1; min-width: 120px; margin-bottom: 20px;">
    <div style="font-size: calc(2em + 1vw); font-weight: bold; color: var(--primary);">40+</div>
    <div style="font-size: 1.2em;">Collaborations</div>
  </div>
  <div style="text-align: center; flex: 1; min-width: 120px; margin-bottom: 20px;">
    <div style="font-size: calc(2em + 1vw); font-weight: bold; color: var(--primary);">4</div>
    <div style="font-size: 1.2em;">Funded Projects</div>
  </div>
</div>

{% include section.html %}

## Highlights

{% capture text %}
Our research focuses on cutting-edge technologies and innovative solutions in the fields of cybersecurity, IoT, and artificial intelligence. We strive to push the boundaries of knowledge and create impactful advancements that address real-world challenges.

{%
include button.html
link="research"
text="See our publications"
icon="fa-solid fa-arrow-right"
flip=true
style="bare"
%}

{% endcapture %}

{%
include feature.html
image="images/photo.jpg"
link="research"
title="Our Research"
text=text
%}

{% capture text %}

We work on a diverse range of projects, from developing novel security solutions to creating advanced AI-powered systems. Our projects aim to solve complex problems and contribute to technological progress across various domains.

{%
include button.html
link="projects"
text="Browse our projects"
icon="fa-solid fa-arrow-right"
flip=true
style="bare"
%}

{% endcapture %}

{%
include feature.html
image="images/photo.jpg"
link="projects"
title="Our Projects"
flip=true
style="bare"
text=text
%}

{% capture text %}

Our team consists of dedicated researchers, talented engineers, and visionary thinkers. Together, we collaborate to drive innovation and make significant contributions to our fields of expertise.

{%  
include button.html
link="team"
text="Meet our team"
icon="fa-solid fa-arrow-right"
flip=true
style="bare"
%}

{% endcapture %}

{%
include feature.html
image="images/photo.jpg"
link="team"
title="Our Team"
text=text
%}

{% capture text %}

We've secured external funding for various research initiatives, working with government agencies and industry partners to develop solutions for real-world problems.

{%
include button.html
link="funding"
text="Explore funded projects"
icon="fa-solid fa-arrow-right"
flip=true
style="bare"
%}

{% endcapture %}

{%
include feature.html
image="images/photo.jpg"
link="funding"
title="Funded Projects"
flip=true
text=text
%}
{% include section.html %}

## Connect With Us

{:.center}

Interested in collaborating or learning more about our research initiatives? We're always looking for talented students, researchers, and industry partners to join our community.

<div style="text-align: center; margin-top: 30px;">
{%
include button.html
link="contact"
text="Get in Touch"
icon="fa-solid fa-envelope"
%}
</div>

<!-- Add viewport meta tag for better mobile rendering -->
<style>
  @media (max-width: 768px) {
    h1 {
      font-size: calc(1.5rem + 2vw);
    }
    h2 {
      font-size: calc(1.3rem + 1vw);
    }
    .feature {
      flex-direction: column !important;
    }
    .feature .feature-image {
      width: 100% !important;
      margin-bottom: 20px;
    }
    .feature .feature-text {
      width: 100% !important;
    }
  }
</style>
