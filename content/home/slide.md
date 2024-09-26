---
title: "슬라이더"
---

<div class="slider" style="position: relative; overflow: hidden;">
  <div class="slide" style="background-image: url('/media/computer.jpg');">
    <div class="content" style="text-align: center;">
      <h2>Mobile Network</h2>
      <p>모바일 네트워크는 이동성과 접근성을 제공하며...</p>
    </div>
  </div>
  <div class="slide" style="background-image: url('/media/LDPC.jpg');">
    <div class="content" style="text-align: left;">
      <h2>LDPC coding</h2>
      <p>Share your knowledge with the group...</p>
    </div>
  </div>
  <div class="slide" style="background-image: url('/media/slice.jpg');">
    <div class="content" style="text-align: right;">
      <h2>Network Slicing</h2>
      <p>Just opened last month!</p>
    </div>
  </div>
  
  <button class="prev" onclick="moveSlide(-1)">&#10094;</button>
  <button class="next" onclick="moveSlide(1)">&#10095;</button>
</div>

<script>
  let currentIndex = 0;
  const slides = document.querySelectorAll('.slide');
  const totalSlides = slides.length;

  function showSlide(index) {
    slides.forEach((slide, i) => {
      slide.style.display = (i === index) ? 'block' : 'none';
    });
  }

  function moveSlide(step) {
    currentIndex = (currentIndex + step + totalSlides) % totalSlides;
    showSlide(currentIndex);
  }

  function autoSlide() {
    currentIndex = (currentIndex + 1) % totalSlides;
    showSlide(currentIndex);
  }

  showSlide(currentIndex);
  setInterval(autoSlide, 3000); // 3초마다 자동 전환
</script>
