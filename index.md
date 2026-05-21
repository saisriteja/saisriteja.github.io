---
layout: default
title: Welcome
---

<div class="intro-page">

  <!-- Hero: profile image + bio -->
  <div class="intro-hero">
    <img src="/img/profile_pic.jpg" alt="Profile Picture" class="profile-image">
    <div class="profile-text">
      <h1 style="font-size:1.7rem;margin-bottom:0.8rem;color:#2D3F50;">K Sai Sri Teja</h1>
      <p>I'm a Machine Learning Engineer at Immerso.ai, where I work on foundational models for large-scale text-to-image and text-to-video generation, with a focus on cinematic movie creation.</p>
      <p>I completed my Master's at IIT Madras, working under <a href="https://www.ee.iitm.ac.in/kmitra/" target="_blank" rel="noopener">Prof. Kaushik Mitra</a>, where my research spanned 2D and 3D vision, particularly in image generation and restoration.</p>
      <p>I'm not big on socializing, but I do enjoy connecting with like-minded people — especially those into computer vision, computational imaging, math, cats, and music. Bonus points if you communicate via funny Instagram reels.</p>
    </div>
  </div>

  <!-- Bottom grid: Explore + Connect -->
  <div class="intro-grid">

    <div class="intro-grid-section">
      <h2>Explore</h2>
      <div class="link-buttons">
        <a href="/research"  class="intro-link-btn">Research</a>
        <a href="/resume"    class="intro-link-btn">Resume</a>
        <a href="/archive"   class="intro-link-btn">Blog Posts</a>
        <a href="/about_me"  class="intro-link-btn">About Me</a>
      </div>
    </div>

    <div class="intro-grid-section">
      <h2>Connect</h2>
      <div class="social-links">
        {% if site.github_username %}
          <a href="https://github.com/{{ site.github_username }}" target="_blank" rel="noopener">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.44 9.8 8.21 11.39.6.11.82-.26.82-.58v-2.03c-3.34.73-4.04-1.61-4.04-1.61-.55-1.39-1.34-1.76-1.34-1.76-1.09-.75.08-.73.08-.73 1.2.08 1.84 1.24 1.84 1.24 1.07 1.83 2.81 1.3 3.5 1 .11-.78.42-1.3.76-1.6-2.67-.3-5.47-1.33-5.47-5.93 0-1.31.47-2.38 1.24-3.22-.12-.3-.54-1.52.12-3.18 0 0 1.01-.32 3.3 1.23A11.5 11.5 0 0 1 12 5.8c1.02.005 2.05.14 3.01.4 2.28-1.55 3.29-1.23 3.29-1.23.66 1.66.24 2.88.12 3.18.77.84 1.24 1.91 1.24 3.22 0 4.61-2.81 5.63-5.48 5.92.43.37.81 1.1.81 2.22v3.29c0 .32.22.7.83.58C20.57 21.8 24 17.31 24 12 24 5.37 18.63 0 12 0z"/></svg>
            GitHub
          </a>
        {% endif %}
        {% if site.linkedin_username %}
          <a href="https://linkedin.com/in/{{ site.linkedin_username }}" target="_blank" rel="noopener">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M20.45 20.45h-3.56v-5.57c0-1.33-.03-3.04-1.85-3.04-1.85 0-2.13 1.44-2.13 2.94v5.67H9.35V9h3.41v1.56h.05c.48-.9 1.64-1.85 3.37-1.85 3.6 0 4.27 2.37 4.27 5.45v6.29zM5.34 7.43a2.07 2.07 0 1 1 0-4.14 2.07 2.07 0 0 1 0 4.14zM7.12 20.45H3.56V9h3.56v11.45zM22.23 0H1.77C.79 0 0 .77 0 1.72v20.56C0 23.23.79 24 1.77 24h20.46c.98 0 1.77-.77 1.77-1.72V1.72C24 .77 23.21 0 22.23 0z"/></svg>
            LinkedIn
          </a>
        {% endif %}
        {% if site.twitter_username %}
          <a href="https://twitter.com/{{ site.twitter_username }}" target="_blank" rel="noopener">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M23.95 4.57a10 10 0 0 1-2.82.77 4.96 4.96 0 0 0 2.16-2.72c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 0 0-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 0 0-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 0 1-2.228-.616v.06a4.923 4.923 0 0 0 3.946 4.827 4.996 4.996 0 0 1-2.212.085 4.936 4.936 0 0 0 4.604 3.417 9.867 9.867 0 0 1-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 0 0 7.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0 0 24 4.59z"/></svg>
            Twitter
          </a>
        {% endif %}
      </div>
    </div>

  </div>
</div>
