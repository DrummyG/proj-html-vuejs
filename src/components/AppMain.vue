<template>
  <main>
    <div class="numeri">
      <div class="box" v-for="(item, index) in numeri" :key="index">
        <p class="bignum">{{ item.numero }}</p>
        <p class="smol">{{ item.testo }}</p>

        <img src="../assets/background-pattern-grid-line-06.png" alt="" />
      </div>
    </div>

    <app-about />

    <app-journey />

    <app-books />

    <section class="sponsor">
      <img
        v-for="(item, index) in immagini"
        :key="index"
        :src="require('../assets/' + item + '.png')"
        alt=""
      />
    </section>

    <app-slider />

    <app-blog />

    <div class="fix">
      <div class="check">
        <i class="fa-solid fa-cat"></i>
        <p>Bottone</p>
      </div>
      <div class="check">
        <i class="fa-solid fa-life-ring"></i>
        <p>Bottone</p>
      </div>
      <div class="check">
        <i class="fa-solid fa-book"></i>
        <p>Bottone</p>
      </div>
      <div class="check">
        <i class="fa-solid fa-cart-shopping"></i>
        <p>Bottone</p>
      </div>
    </div>
  </main>
</template>

<script>
import AppAbout from "./AppAbout.vue";
import AppJourney from "./AppJourney.vue";
import AppBooks from "./AppBooks.vue";
import AppSlider from "./AppSlider.vue";
import AppBlog from "./AppBlog.vue";

export default {
  name: "AppMain",
  components: {
    AppAbout,
    AppJourney,
    AppBooks,
    AppSlider,
    AppBlog,
  },
  data() {
    return {
      numeri: [
        {
          numero: "1.926",
          testo: "finished session",
        },
        {
          numero: "100%",
          testo: "satisfaction rate",
        },
        {
          numero: "3092+",
          testo: "enrolled learners",
        },
        {
          numero: "200",
          testo: "online instructors",
        },
      ],
      immagini: [
        "client-logo-05-primary",
        "client-logo-06-primary",
        "client-logo-07-primary",
        "client-logo-04-primary",
        "client-logo-03-primary",
        "client-logo-02-primary",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";

.numeri {
  margin: 80px auto;
  display: flex;
  justify-content: center;

  .box {
    position: relative;
    text-align: center;
    width: 250px;

    .bignum {
      font-size: xx-large;
      font-weight: bold;
      color: $button;
    }

    .smol {
      text-transform: uppercase;
      font-size: small;
      font-weight: bold;
    }

    img {
      position: absolute;
      left: 0;
      top: 0;
    }
  }
}

.sponsor {
  display: flex;
  justify-content: space-between;
  align-items: center;

  img {
    filter: grayscale(100%);
    opacity: 0.4;
  }
}

.fix {
  position: fixed;
  top: 50%;
  right: -10px;
  z-index: 100;
  background-color: $color-footer;
  border-radius: 20px;

  .check{
    border-radius: 20px;
    position: relative;
    z-index: 30;

    i:hover{
      color: $button;
    }

    i{
      border-radius: 5px;
      font-size: x-large;
      padding: 10px;
      padding-right: 20px;
      z-index: 30;
      background-color: $color-footer;
    }

    p{
      padding: 5px;
      color: $color-footer;
      background-color: $footer;
      position: absolute;
      right: -100px;
      top: 10px;
      transition: all 1s;
      z-index: -1;
      border-radius: 5px;
    }

    i:hover + p{
      right: 70px;
    }
  }
}
</style>