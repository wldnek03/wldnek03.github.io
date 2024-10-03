---
# Use the Intro widget of the Blog template
widget: about.avatar

# This file represents a page section.
headless: true

# Order that this section will appear in.
weight: 10

author: admin

#design:
#  background:
#    color: '#090a0b'
#    text_color_light: true
#    video:
#      path:  # enter filename of a video in /assets/media
#  css_class: fullscreen
---
<div class="carousel-container">
  <div class="carousel-slide">
    <input type="radio" name="carousel" id="slide1" checked>
    <input type="radio" name="carousel" id="slide2">
    <input type="radio" name="carousel" id="slide3">

    <div class="carousel-content">
      <div class="carousel-item" style="background-image: url('/media/LDPC.jpg');">
        <h2>LDPC</h2>
        <p>프로제트 내용적기</p>
      </div>
      <div class="carousel-item" style="background-image: url('/media/computer.jpg');">
        <h2>Mobile computer</h2>
        <p>모바일 네트워크는 이동성과 접근성을 제공하며, 5G 기술의 발전으로 빠르고 효율적인 통신을 가능하게 하여 미래의 네트워크 혁신을 이끌고 있습니다.</p>
      </div>
      <div class="carousel-item" style="background-image: url('/media/slice.jpg');">
        <h2>Network Slicing</h2>
        <p>내용적기</p>
      </div>
    </div>

    <div class="carousel-controls">
      <label for="slide1"></label>
      <label for="slide2"></label>
      <label for="slide3"></label>
    </div>
  </div>
</div>

<style>
.carousel-container {
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
  position: relative;
}

.carousel-slide {
  display: flex;
  overflow: hidden;
  position: relative;
}

.carousel-content {
  display: flex;
  width: 300%;
  transition: transform 0.5s ease;
}

.carousel-item {
  width: 100%;
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 400px;
  color: white;
  text-align: center;
}

input[type="radio"] {
  display: none;
}

input#slide1:checked ~ .carousel-content {
  transform: translateX(0%);
}

input#slide2:checked ~ .carousel-content {
  transform: translateX(-33.33%);
}

input#slide3:checked ~ .carousel-content {
  transform: translateX(-66.66%);
}

.carousel-controls {
  position: absolute;
  bottom: 10px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: 10px;
}

.carousel-controls label {
  display: inline-block;
  width: 10px;
  height: 10px;
  background-color: white;
  border-radius: 50%;
  cursor: pointer;
}

.carousel-controls label:hover {
  background-color: #999;
}
</style>

👋 Hi, I'm **Jiwoo**. I'm doing research regarding communications and networks.
{style="font-size: 1.2rem; background: #FFB76B; background: linear-gradient(to right, #FFB76B 0%, #FFA73D 30%, #FF7C00 60%, #FF7F04 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent;"}


Check out my [resume](about/) and the portfolio below.✔️
