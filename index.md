---
header: images/background.jpg
header-dark: true
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

<div class="news-carousel-container" style="max-width: 100%; margin: 30px auto; position: relative; overflow: hidden;">
  <div class="news-carousel" style="display: flex; transition: transform 0.8s ease; width: 100%;">
    {% for post in site.posts limit:15 %}
      <div class="carousel-item" style="min-width: 33.33%; padding: 0 15px; box-sizing: border-box;">
        <div style="border-radius: 8px; overflow: hidden; box-shadow: 0 4px 12px rgba(0,0,0,0.1); height: 100%;">
          {% if post.image %}
          <div style="height: 180px; overflow: hidden;">
            <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" style="width: 100%; height: 100%; object-fit: cover;">
          </div>
          {% else %}
          <div style="height: 180px; background-color: #f0f0f0; display: flex; align-items: center; justify-content: center;">
            <i class="fa-regular fa-newspaper" style="font-size: 40px; color: #888;"></i>
          </div>
          {% endif %}
          <div style="padding: 20px;">
            <p style="color: #666; margin-bottom: 5px; font-size: 0.9em;">{{ post.date | date: "%b %d, %Y" }}</p>
            <h3 style="margin-top: 0; font-size: 1.2em; line-height: 1.3; overflow: hidden; text-overflow: ellipsis; display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical;">
              <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: inherit;">{{ post.title }}</a>
            </h3>
            <p style="font-size: 0.9em; margin-bottom: 8px; overflow: hidden; text-overflow: ellipsis; display: -webkit-box; -webkit-line-clamp: 3; -webkit-box-orient: vertical;">{{ post.excerpt | strip_html | truncate: 100 }}</p>
            <a href="{{ post.url | relative_url }}" style="font-weight: 500; display: inline-block;">Read more →</a>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
  
  <button onclick="moveCarousel(-1)" style="position: absolute; left: 10px; top: 50%; transform: translateY(-50%); background: rgba(255,255,255,0.8); border: none; border-radius: 50%; width: 40px; height: 40px; display: flex; align-items: center; justify-content: center; cursor: pointer; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">
    <i class="fa-solid fa-chevron-left"></i>
  </button>
  
  <button onclick="moveCarousel(1)" style="position: absolute; right: 10px; top: 50%; transform: translateY(-50%); background: rgba(255,255,255,0.8); border: none; border-radius: 50%; width: 40px; height: 40px; display: flex; align-items: center; justify-content: center; cursor: pointer; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">
    <i class="fa-solid fa-chevron-right"></i>
  </button>
</div>

<div style="text-align: center; margin-top: 20px;">
{%
include button.html
link="blog"
text="View All News"
icon="fa-solid fa-newspaper"
%}
</div>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    // Carousel variables
    let currentIndex = 0;
    const items = document.querySelectorAll('.carousel-item');
    const totalItems = items.length;
    const visibleItems = 3;  // Show 3 items at once
    let carouselInterval;
    
    // Calculate max index (accounting for 3 visible items)
    const maxIndex = Math.max(0, totalItems - visibleItems);

    // Initialize carousel
    updateCarousel();
    startAutoScroll();

    // Make functions available globally
    window.moveCarousel = function(direction) {
      currentIndex = Math.min(Math.max(0, currentIndex + direction), maxIndex);
      updateCarousel();
      resetAutoScroll();
    };

    function updateCarousel() {
      const carousel = document.querySelector('.news-carousel');
      carousel.style.transform = `translateX(-${currentIndex * 33.33}%)`;
    }

    function startAutoScroll() {
      // Move to next slide every 4 seconds
      carouselInterval = setInterval(() => {
        if (currentIndex < maxIndex) {
          currentIndex++;
        } else {
          currentIndex = 0;
        }
        updateCarousel();
      }, 4000);
    }

    function resetAutoScroll() {
      clearInterval(carouselInterval);
      startAutoScroll();
    }
  });
</script>

{% include section.html %}

## Key Statistics
{:.center}

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 30px; margin: 40px 0;">
  <div style="text-align: center; flex: 1; min-width: 200px;">
    <div style="font-size: 3em; font-weight: bold; color: var(--primary);">25+</div>
    <div style="font-size: 1.2em;">Research Publications</div>
  </div>
  <div style="text-align: center; flex: 1; min-width: 200px;">
    <div style="font-size: 3em; font-weight: bold; color: var(--primary);">15+</div>
    <div style="font-size: 1.2em;">Ongoing Projects</div>
  </div>
  <div style="text-align: center; flex: 1; min-width: 200px;">
    <div style="font-size: 3em; font-weight: bold; color: var(--primary);">40+</div>
    <div style="font-size: 1.2em;">Collaborations</div>
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