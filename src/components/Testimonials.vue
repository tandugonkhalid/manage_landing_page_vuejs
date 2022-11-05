<template>
  <div class="testimonials">
    <h1>What they've said</h1>
    <div class="carousel slide">
      <div class="item fade">
        <img src="images/avatar-anisha.png" alt="Anisha Li" />
        <h5>Anisha Li</h5>
        <p>
          "Manage has supercharged our team's workflow. The ability to maintain
          visibility on larger milestone at all times keeps everyone motivated."
        </p>
      </div>

      <div class="item fade">
        <img src="images/avatar-ali.png" alt="Anisha Li" />
        <h5>Ali Bravo</h5>
        <p>
          "We have been able to cancel so many other subscriptions since using
          Manage. There is no more cross-channel confusion and everyone is much
          more focused"
        </p>
      </div>

      <div class="item fade">
        <img src="images/avatar-richard.png" alt="Anisha Li" />
        <h5>Richard Watts</h5>
        <p>
          "Manage allows us to provide structure and process. It keeps us
          organized and focused. I can't stop recommending them to everyone I
          talk to!"
        </p>
      </div>

      <div class="item fade">
        <img src="images/avatar-shanai.png" alt="Anisha Li" />
        <h5>Shanai Gough</h5>
        <p>
          "Their software allows us to track, manage and collaborate on our
          projects from anywhere. It keeps the whole team in-sync without being
          intrusive."
        </p>
      </div>

      <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
      <a class="next" onclick="plusSlides(1)">&#10095;</a>

      <div style="text-align: center">
        <span class="dot" onclick="currentSlide(1)"></span>
        <span class="dot" onclick="currentSlide(2)"></span>
        <span class="dot" onclick="currentSlide(3)"></span>
        <span class="dot" onclick="currentSlide(4)"></span>
      </div>
    </div>

    <button type="submit">Get Started</button>
  </div>
</template>

<script>
// import carousel from 'vue-owl-carousel';
export default {
  name: "Testimonials",
};

var slideIndex = 0;
showSlides();

// function plusSlides(n) {
//   showSlides(slideIndex += n);
// }

// // Thumbnail image controls
// function currentSlide(n) {
//   showSlides(slideIndex = n);
// }

function showSlides() {
  var i;
  var slides = document.getElementsByClassName("item");
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  slideIndex++;
  if (slideIndex > slides.length) {
    slideIndex = 1;
  }
  slides[slideIndex - 1].style.display = "block";
  setTimeout(showSlides, 50000); // Change image every 2 seconds
}
</script>

<style lang="scss" scoped>
@import "../css/__colors.scss";
@import "../css/__fonts.scss";

.testimonials {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

h1 {
  font-size: 2em;
}

.card {
  background-color: map-get($colors, dark-grayish-blue);
}

.carousel {
  max-width: 1000px;
  position: relative;
  margin: auto;
}

.item {
  display: none;
  background-color: map-get($colors , very-light-gray );
}

.fade{
    display: flex;
    justify-content: center;
    align-items: center;

    p{
        width: 500px;
    }
}

.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  margin-top: -22px;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}

.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active,
.dot:hover {
  background-color: #717171;
}

.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}

@keyframes fade {
  from {
    opacity: 4;
  }
  to {
    opacity: 1;
  }
}
</style>
