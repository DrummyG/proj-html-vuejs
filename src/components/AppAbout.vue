<template>
  <section>
    <p class="mini-title">about me</p>
    <div class="d-flex align-items-center justify-content-between space">
      <p class="font-diff big">
        How to Be an Alpha Male: The 15 Habits of True Alphas
      </p>
      <div class="right">
        <p class="question">
          Want to learn how to be an <span>alpha male</span>? How to be more
          masculine? how to be the man you always wanted to be?
        </p>
        <p class="answer">
          your goal is to show consistency on business, core values, and
          customer care. Punctuality, responsability, individuality, accuracy,
          enthusiasm - you have to clearly explain how these qualities are
          applicable to your word. And the important thing is that you do love
          what you do.
        </p>
      </div>
    </div>

    <div class="d-flex align-items-center justify-content-between space">
      <div class="video">
        <img
          src="../assets/home-movation-video-poster-670x450.jpg"
          alt=""
          class="preview"
        />
        <img src="../assets/icon-youtube-play.png" alt="" class="icon" />
      </div>

      <div class="description">
        <p class="font-diff medium">
          "Every morning you have two choices: continue to sleep with your
          dreams, or wake uo and chase them."
        </p>
        <img src="../assets/home-movation-shape-01.png" alt="">
        <p class="name">Kaixa Stark</p>
        <p class="occupation">Wingman</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppAbout",
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";
section {
  width: 70%;
  margin: 60px auto;

  .space {
    margin: 60px 0;
  }

  .mini-title {
    text-transform: uppercase;
    font-size: smaller;
    color: $button;
  }

  .big {
    width: 40%;
    font-size: 35px;
  }

  .right {
    width: 50%;

    .question {
      font-weight: bold;

      span {
        color: $button;
      }
    }

    .answer {
      font-size: small;
      color: $grey-text;
    }
  }

  .video {
    position: relative;

    .preview {
      width: 600px;
      border-radius: 5px;
    }

    .icon {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }

  .description {
      width: 25%;

      .medium{
          font-size: 20px;
          margin-bottom: 40px;
      }

      .name{
          text-transform: uppercase;
          margin-top: 20px;
      }

      .occupation{
          text-transform: uppercase;
          color: $grey-text;
          font-size: smaller;
      }
  }
}
</style>