<template>
  <div class="container">
    <img
      src="images/bg-simplify-section-desktop.svg"
      alt=""
      class="bg-design"
    />
    <Navbar />
    <Hero />
    <Testimonials />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Hero from './components/Hero.vue';
import Testimonials from "./components/Testimonials.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Hero,
    Testimonials
  },
};
</script>

<style lang="scss">
@import "./css/__colors.scss";
@import "./css/__fonts.scss";

*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

.container {
  position: relative;
  height: 100vh;
}

.bg-design {
  width: 100%;
  position: absolute;
  z-index: -1;
}

button {
  padding: 0.7rem;
  border: none;
  border-radius: 50px;
  width: 10em;
  background-color: map-get($colors, bright-red);
  color: map-get($colors, very-pale-red);
  font-family: "Be Vietnam", sans-serif;
  font-weight: 700;
  box-shadow: 0 5px 15px map-get($colors, bright-red);
  transition: 0.5s ease;

  &:hover {
    cursor: pointer;
    opacity: 0.8;
  }
}

h1{
        color: map-get($colors , very-dark-blue );
        font-size: 3em;
        font-weight: 700;
        font-family: "Be Vietnam", sans-serif;
        line-height: 1.3em;
        margin-bottom: 30px;
    }
</style>
