---
layout: default
title: Home
---

<!-- Hero Section -->
<section class="hero">
    <div class="hero-content">
        <h1 class="hero-title">Welcome to My Blog</h1>
        <p class="hero-subtitle">Exploring ideas, sharing knowledge, and creating value</p>
        <a href="#featured" class="cta-button">Read Latest Posts</a>
    </div>
</section>

<!-- Featured Posts -->
<section id="featured" class="featured-posts">
    <h2 class="section-title">Featured Posts</h2>
    <div class="post-grid">
        {% for post in site.posts limit:3 %}
        <article class="post-card">
            {% if post.image %}
            <img src="{{ post.image }}" alt="{{ post.title }}" class="post-image">
            {% endif %}
            <div class="post-content">
                <h3 class="post-title">{{ post.title }}</h3>
                <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
                <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
            </div>
        </article>
        {% endfor %}
    </div>
</section>

<!-- About Section -->
<section class="about">
    <div class="about-content">
        <h2 class="section-title">About Me</h2>
        <p>Hello! I'm a passionate writer and developer sharing my thoughts and experiences.</p>
        <div class="social-links">
            <a href="#" class="social-link"><i class="fab fa-github"></i></a>
            <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
            <a href="#" class="social-link"><i class="fab fa-linkedin"></i></a>
        </div>
    </div>
</section>