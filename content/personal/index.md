---
title: "El Cocuy"
author: "Nancy A. Daza-Báez"
description: "Photos and reflections from El Cocuy, Boyacá, Colombia."
disableAnchoredHeadings: false
---

El Cocuy is a small town nestled in the eastern range of the Colombian Andes, in the department of Boyacá. With a population of around 4,300 inhabitants, it sits at the foot of the Sierra Nevada del Cocuy, one of the most spectacular mountain ranges in South America, and is home to dramatic páramo landscapes, glaciers, and a rich cultural heritage. **It is where I was born, where I grew up, and where my roots are.**

<style>
.photo-carousel { overflow-x: auto; display: flex; scroll-snap-type: x mandatory; scrollbar-width: none; -ms-overflow-style: none; margin-top: 1.5rem; }
.photo-carousel::-webkit-scrollbar { display: none; }
.photo-carousel figure { margin: 0; flex: 0 0 100%; scroll-snap-align: start; }
.photo-carousel img { width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3; display: block; }
.photo-carousel figcaption { font-size: 0.85rem; color: #666; margin-top: 6px; text-align: center; }
.carousel-dots { display: flex; justify-content: center; gap: 8px; margin-top: 10px; }
.carousel-dots span { width: 8px; height: 8px; border-radius: 50%; background: #ccc; cursor: pointer; transition: background 0.3s; display: inline-block; }
.carousel-dots span.active { background: #555; }
#c-mahoma img { aspect-ratio: 16/9; }
#c-around img { aspect-ratio: 4/1; }
#c-town figure:nth-child(1) img, #c-town figure:nth-child(2) img { aspect-ratio: 1/1; }
</style>

---

## Cerro de Mahoma

Cerro de Mahoma is a hill that rises to 4,040 metres above sea level, just beside the town of El Cocuy — on the opposite side from the Sierra Nevada. It is the town's most beloved viewpoint, offering a sweeping panorama of the surrounding municipalities and páramo landscape. The hill also carries local legend: it is said that the mohán, a mythical figure of Colombian folklore, inhabits there.

<div class="photo-carousel" id="c-mahoma">
  <figure>
    <img src="/photos/el-cocuy/93041DE3-F192-4AC1-B521-3A1121C3B6BF_1_105_c.jpeg" alt="Panoramic view from Cerro de Mahoma">
    <figcaption>Panoramic view from Cerro de Mahoma</figcaption>
  </figure>
  <figure>
    <img src="/photos/el-cocuy/D1267616-BDFD-467E-AACD-0507B53C7050_1_105_c.jpeg" alt="Valley view from Cerro de Mahoma">
    <figcaption>Valley view from Cerro de Mahoma</figcaption>
  </figure>
</div>
<div class="carousel-dots" id="d-mahoma"></div>

---

## The Town

El Cocuy sits at around 2,750 metres above sea level, surrounded by green hills and fertile valleys. Its colonial church, small plazas, and close-knit community make it one of the most charming towns in Boyacá.

<div class="photo-carousel" id="c-town">
  <figure>
    <img src="/photos/el-cocuy/IMG_1826.JPG" alt="El Cocuy seen from above">
    <figcaption>El Cocuy from above</figcaption>
  </figure>
  <figure>
    <img src="/photos/el-cocuy/IMG_1859.JPG" alt="Church of El Cocuy">
    <figcaption>Parish church, El Cocuy</figcaption>
  </figure>
  <figure>
    <img src="/photos/el-cocuy/IMG_3676.JPG" alt="El Cocuy town nestled in the valley">
    <figcaption>El Cocuy nestled in the valley</figcaption>
  </figure>
</div>
<div class="carousel-dots" id="d-town"></div>

### Around Town

<div class="photo-carousel" id="c-around">
  <figure>
    <img src="/photos/el-cocuy/IMG_3725.JPG" alt="Laguna del Palchacual">
    <figcaption>Laguna del Palchacual</figcaption>
  </figure>
  <figure>
    <img src="/photos/el-cocuy/IMG_3791.JPG" alt="Laguna del Palchacual">
    <figcaption>Laguna del Palchacual</figcaption>
  </figure>
</div>
<div class="carousel-dots" id="d-around"></div>

---

## Sierra Nevada del Cocuy

The Sierra Nevada del Cocuy is one of the most important glacial massifs in Colombia, with peaks reaching over 5,000 metres. Its glaciers, lagoons, and frailejones páramo are protected within the Parque Nacional Natural El Cocuy.

<div class="photo-carousel" id="c-sierra">
  <figure>
    <img src="/photos/el-cocuy/5788B446-E9BA-459F-B3F7-0A35C8942455_1_105_c.jpeg" alt="Sierra Nevada del Cocuy with frailejones">
    <figcaption>Sierra Nevada del Cocuy, with frailejones in the foreground</figcaption>
  </figure>
  <figure>
    <img src="/photos/el-cocuy/IMG_3919.JPG" alt="Parque Nacional Natural El Cocuy, Sitio Lajas at 4700m">
    <figcaption>Parque Nacional Natural El Cocuy — Sitio Lajas, 4,700 m</figcaption>
  </figure>
  <figure>
    <img src="/photos/el-cocuy/IMG_3838.JPG" alt="On the glacier of the Sierra Nevada del Cocuy">
    <figcaption>On the glacier</figcaption>
  </figure>
  <figure>
    <img src="/photos/el-cocuy/P1050798.JPG" alt="Rock formation emerging from mist and glacier">
    <figcaption>Pulpito del Diablo</figcaption>
  </figure>
  <figure>
    <img src="/photos/el-cocuy/P1050632.JPG" alt="Hikers climbing the glacier in fog">
    <figcaption>Climbing the glacier</figcaption>
  </figure>
  <figure>
    <img src="/photos/el-cocuy/PASEO%20COCUY%202006%20(13).jpg" alt="Glacier and rocky terrain, 2006">
    <figcaption>Ritak U'wa Blanco, 2006</figcaption>
  </figure>
</div>
<div class="carousel-dots" id="d-sierra"></div>

<script>
function initCarousel(carouselId, dotsId) {
  const carousel = document.getElementById(carouselId);
  const dotsEl = document.getElementById(dotsId);
  const count = carousel.querySelectorAll('figure').length;
  for (let i = 0; i < count; i++) {
    const dot = document.createElement('span');
    if (i === 0) dot.classList.add('active');
    dot.addEventListener('click', () => {
      carousel.scrollTo({ left: carousel.offsetWidth * i, behavior: 'smooth' });
    });
    dotsEl.appendChild(dot);
  }
  carousel.addEventListener('scroll', () => {
    const idx = Math.round(carousel.scrollLeft / carousel.offsetWidth);
    dotsEl.querySelectorAll('span').forEach((d, i) => d.classList.toggle('active', i === idx));
  });
}
initCarousel('c-mahoma', 'd-mahoma');
initCarousel('c-town',   'd-town');
initCarousel('c-around', 'd-around');
initCarousel('c-sierra', 'd-sierra');
</script>
