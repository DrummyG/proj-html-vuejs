<template>
  <section>
    <p class="smol-title">Blog Updates</p>
    <p class="big-text font-diff">
      Interesting <span>articles update</span> daily
    </p>
    <div class="box">
      <div class="card" v-for="(item, index) in blogs" :key="index">
        <img :src="require('../assets/' + item.img + '.jpg')" alt="" />
        <p class="date"><i class="fa-solid fa-calendar"></i> May 13, 2020</p>
        <p class="course-name">{{ item.title }}</p>
        <p class="course-desc">{{ item.desc }}</p>
      </div>
    </div>
    <p class="all">View all posts</p>
  </section>
</template>

<script>
export default {
  name: "AppBlog",
  data() {
    return {
      blogs: [
        {
          img: "motivation-blog-04-480x325",
          title: "How to Stay True to Your Personal Brand",
          desc: "When it comes to your business o career, you want ...",
        },
        {
          img: "motivation-blog-03-480x325",
          title: "5 Vita Lessons in 5 Years of Freelancing",
          desc: "Being self-employed and working from home, it's easy to get ...",
        },
        {
          img: "motivation-blog-02-480x325",
          title: "11 Super Useful Tips for Small-Business Owner",
          desc: "Being a small-business owners poses a ton of challenges, We ...",
        },
        {
          img: "motivation-blog-01-480x325",
          title: "How To GIve Yourself Grace To Start Again",
          desc: "Forgive yourself for bad habits you may have started or ...",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";

.smol-title {
  font-size: smaller;
  text-transform: uppercase;
  color: $grey-text;
}

.big-text {
  color: $cards;
  font-size: 40px;

  span {
    color: $button;
  }
}

.box {
  display: flex;
  gap: 20px;

  .card {
    border: 0;

    .date {
      color: $grey-text;
      font-size: small;
      margin: 10px 0;
    }

    .course-name {
      font-size: 20px;
      font-weight: bold;
    }

    .course-desc{
        font-size: small;
        color: $grey-text;
    }
  }
}

.all{
    font-size: smaller;
    text-transform: uppercase;
    text-align: center;
    color: $button;
    text-decoration: underline;
}
</style>