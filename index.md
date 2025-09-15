---
layout: default
title: Home
---

{% include nav.html %}
<link rel="stylesheet" href="/assets/css/custom.css">
<img class="header-logo" src="/assets/images/vinniskitchen-logo.png" alt="Vinni's Kitchen logo">

# Vinni’s Kitchen
Homestyle Indian food and catering. Lady-owned, community-loved.

<!-- Image Slider -->
<div class="section">
  <div class="slider" id="foodSlider">
    <!-- Replace these with your own images in /assets/images/home/ -->
    <div class="slide active"><img src="/assets/images/home/slide1.jpg" alt="Vinni's Kitchen dish 1"></div>
    <div class="slide"><img src="/assets/images/home/slide2.jpg" alt="Vinni's Kitchen dish 2"></div>
    <div class="slide"><img src="/assets/images/home/slide3.jpg" alt="Vinni's Kitchen dish 3"></div>
  </div>
</div>

<div class="section">
  <div class="grid">
    <div class="card">
      <h3>PreOrders</h3>
      <p>Order this week’s meals for delivery.</p>
      <a href="/preorders/">Open PreOrders →</a>
    </div>
    <div class="card">
      <h3>Catering</h3>
      <p>Parties, housewarmings, and community events—made easy.</p>
      <a href="/catering-request/">Request catering →</a>
    </div>
    <div class="card">
      <h3>Our Recipes</h3>
      <p>Homestyle dishes from our kitchen to yours.</p>
      <a href="/recipes/">Browse recipes →</a>
    </div>
  </div>
</div>

<!-- Reviews Slider -->
<div class="section">
  <h2>What customers say</h2>
  <div class="review-slider" id="reviewSlider">
    {% for r in site.data.reviews %}
    <div class="review{% if forloop.first %} active{% endif %}">
      <p>“{{ r.text }}”</p>
      <div class="who">— {{ r.author }}{% if r.stars %} • ⭐ {{ r.stars }}/5{% endif %}</div>
      {% if r.link %}<p><a href="{{ r.link }}" target="_blank" rel="noopener">View on Google</a></p>{% endif %}
    </div>
    {% endfor %}
  </div>
</div>

<script>
(function(){
  // Image slider (change every 3s)
  const slides = document.querySelectorAll('#foodSlider .slide');
  let i = 0;
  setInterval(()=>{ slides[i].classList.remove('active'); i = (i+1)%slides.length; slides[i].classList.add('active'); }, 3000);

  // Reviews slider (change every 5s)
  const revs = document.querySelectorAll('#reviewSlider .review');
  let j = 0;
  setInterval(()=>{ revs[j].classList.remove('active'); j = (j+1)%revs.length; revs[j].classList.add('active'); }, 5000);
})();
</script>