<template>
  <div class="box">
    <div
      v-for="(item, index) in datiSlider"
      :key="index"
      :class="index === counter ? 'left active' : 'left'"
    >
      <p class="mini-title">Real Stories</p>
      <p class="story">{{ item.esperienza }}</p>
      <img :src="require('../assets/' + item.img + '.jpg')" alt="" />
      <p>{{ item.nome }}</p>
      <p class="job">/{{ item.occupazione }}</p>
    </div>

    <div class="palla">
      <i class="fa-solid fa-caret-up" @click="up"></i>
      <p>{{ counter + 1 }}/4</p>
      <i class="fa-solid fa-caret-down" @click="down"></i>
    </div>

    <img src="../assets/home-movation-testimonial-image-768x562.jpg" alt="" />
  </div>
</template>

<script>

export default {
  name: "AppSlider",
  data() {
    return {
      datiSlider: [
        {
          esperienza:
            "I am free to learn at my own pace, follow my own schedule and choose the subject i want to learn from the syllabus. great study portal for people like me",
          img: "testimonial-avata-02",
          nome: "Mina Hollace",
          occupazione: "Freelance",
        },
        {
          esperienza:
            "I like my woman like my coffe: without other people's dick in it ",
          img: "testimonial-avata-03",
          nome: "Giovanni Muchacha",
          occupazione: "Social media manager",
        },
        {
          esperienza:
            "I was a Sigma Man, but now i can understand the power of toxic masculinity",
          img: "testimonial-avata-04",
          nome: "Kyle Jenner",
          occupazione: "Student",
        },
        {
          esperienza:
            "I was a Sigma Man, but now i can understand the power of toxic masculinity",
          img: "testimonial-avata-01",
          nome: "Kyle Jenner the 2nd",
          occupazione: "Student",
        },
      ],
      counter: 0,
    };
  },
  methods: {
    up() {
         this.counter++;
      if (this.counter === 4) {
        this.counter = 0;
      }
      console.log(this.counter);
    },
    down() {
         this.counter--;
      if (this.counter === -1) {
        this.counter = 3;
      }
      console.log(this.counter);
    },
  },
  mounted() {
    setInterval(() => {
      this.counter++;
      if (this.counter === 4) {
        this.counter = 0;
      }
      console.log(this.counter);
    }, 4000);
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";

.box {
  height: 450px;
  display: flex;
  overflow: hidden;
  position: relative;
  background-image: url("../assets/background-pattern-wavify.png");
  background-color: $hero-back;

  .left {
    position: absolute;
    left: 0;
    top: -500px;
    width: 50%;
    height: 100%;
    background-image: url("../assets/background-pattern-wavify.png");
    background-color: $hero-back;
    transition: 2s all;
    text-align: center;

    .mini-title {
      font-size: smaller;
      text-transform: uppercase;
      margin-top: 60px;
      color: $grey-text;
    }

    .story {
      width: 50%;
      margin: 30px auto;
      font-size: large;
    }

    .job {
      font-size: x-small;
    }

    img {
      width: 70px;
      height: 70px;
      border-radius: 50%;
      margin-left: 0;
      margin-bottom: 20px;
    }
  }

  .palla {
    background-color: white;
    width: 70px;
    height: 70px;
    position: absolute;
    top: 225px;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 100;
    border-radius: 50%;
    display: flex;
    flex-flow: column;
    align-items: center;
    justify-items: center;
    gap: 5px;

    p {
      margin: 0;
      text-align: center;
      font-size: large;
    }

    i {
      color: $grey-text;
    }
  }

  .active {
    top: 0;
  }

  img {
    margin-left: 50%;
    height: 100%;
    width: 50%;
    object-fit: cover;
  }
}
</style>