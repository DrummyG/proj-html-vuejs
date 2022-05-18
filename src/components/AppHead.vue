<template>
  <header id="#top">
    <app-nav />

    <div class="container">
      <div class="jumbo-text">
        <p class="caption">i'm wingman</p>
        <h1 class="font-diff">Peace On Earth A Wonderful Wish But No Way</h1>
        <p>
          Success isn't overnight. It's when everyday you get a little better
          than the day before. It all adds up.
        </p>
        <button>Get started for free <i class="fa-solid fa-arrow-right"></i></button>
      </div>
    </div>

    <img src="../assets/home-movation-hero-image.png" alt="" class="face" />
    <img src="../assets/home-movation-shape-face-300x267.png" alt="" />
  </header>
</template>

<script>
import AppNav from "./AppNav.vue";

export default {
  name: "AppHead",
  props: {},
  components: {
    AppNav,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/styles/variables.scss";
header {
  height: 600px;
  background-color: $hero-back;
  background-image: url("../assets/background-pattern-wavify.png");
  position: relative;

  .jumbo-text{
    width: 30%;
    height: 500px;
    margin-left: 50px;
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: flex-start;

    .caption{
      text-transform: uppercase;
      font-weight: bolder;
    }

    p{
      font-size: small;
    }

    h1{
      font-size: 45px;
    }
  }

  img {
    position: absolute;
    bottom: 0;
    right: 20%;
  }

  .face {
    height: 80%;
    z-index: 10;
  }
}
</style>
