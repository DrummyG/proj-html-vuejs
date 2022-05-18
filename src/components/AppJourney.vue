<template>
  <section>
    <p class="mini-title">begin your journey at maxcoach</p>
    <p class="big-title font-diff">Latest <span>Online Courses</span></p>
    <div class="container">
      <div class="row">
        <div class="col-4 journey" v-for="(item, index) in lessons" :key="index">
          <img :src="require('../assets/' + item.img + '.jpg')" alt="" />
          <div class="data">
            <p class="prezzo">
              &#36;{{ item.price }}.<span>{{ item.cents }}</span>
            </p>
            <p class="course-name">{{ item.title }}</p>
            <div class="bot">
              <p><i class="fa-solid fa-file"></i> {{ item.number }} Lessons</p>
              <p><i class="fa-solid fa-user"></i> 50 students</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <button>View all courses <i class="fa-solid fa-arrow-right"></i></button>
  </section>
</template>

<script>
export default {
  name: "AppJourney",
  data() {
    return {
      lessons: [
        {
          img: "motivation-course-06-480x298",
          title: "How to be Successful: Create a Growth Mindset for Success",
          price: "30",
          cents: "00",
          number: "3",
        },
        {
          img: "motivation-course-05-480x298",
          title: "How to build Confidence in your Abilities",
          price: "30",
          cents: "00",
          number: "1",
        },
        {
          img: "motivation-course-04-480x298",
          title: "Productivity Machine - Focus in a Distracted World",
          price: "20",
          cents: "00",
          number: "5",
        },
        {
          img: "motivation-course-03-480x298",
          title: "Effective Time Managment Mastery - Complete Guide",
          price: "20",
          cents: "00",
          number: "18",
        },
        {
          img: "motivation-course-02-480x298",
          title: "Body Language Secrets for Enterpreneur",
          price: "25",
          cents: "99",
          number: "19",
        },
        {
          img: "motivation-course-01-480x298",
          title: "Management Skills: the Science of Leadership",
          price: "19",
          cents: "99",
          number: "17",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";
section {
  color: $cards;

  .mini-title {
    font-size: smaller;
    color: $grey-text;
    text-align: center;
    text-transform: uppercase;
  }

  .big-title {
    text-align: center;
    font-size: 45px;

    span {
      color: $button;
    }
  }

  .data{
      padding-left: 10px;
  }

  .prezzo {
    margin-top: 10px;
    font-size: x-large;
    color: $button;
    font-weight: bold;

    span {
      font-size: large;
    }
  }

  .course-name {
    font-size: 20px;
    font-weight: bold;
  }

  .bot{
      display: flex;
      gap: 30px;
      font-size: smaller;
      color: $grey-text;
      margin-bottom: 40px;
  }

  img {
      margin-top: 40px;
    width: 100%;
    border-radius: 5px;
  }

  button{
      margin: 50px auto;
      position: relative;
      left: 50%;
      top: 0;
      transform: translate(-50%, 0);
  }
}
</style>