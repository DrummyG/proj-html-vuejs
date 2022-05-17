<template>
  <section>
    <div class="testo">
      <p class="smol-title">book store online</p>
      <p class="big-title font-diff">Be Alpha Whith <span>Wingman's Book</span></p>

      <p><i class="fa-solid fa-check"></i> Help you understand yourself better</p>
      <p><i class="fa-solid fa-check"></i> Revealing mature tips</p>
      <p><i class="fa-solid fa-check"></i> Give the right advice</p>
      <p><i class="fa-solid fa-check"></i> Fascinating examples of Alpha Man</p>
      <button>Get Free Ebook</button>
    </div>

    <div class="books">
      <div class="cover">
        <img src="../assets/product-book-11-400x400.jpg" alt="" />
        <p class="titolo">Alpha Man by Maxcoach</p>
        <p class="prezzo">&#36;29.<span>00</span></p>
      </div>
      <div class="cover">
        <img src="../assets/product-book-10-400x400.jpg" alt="" />
        <p class="titolo">Real Man 4.0 by Maxcoach</p>
        <p class="prezzo">&#36;39.<span>00</span></p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppBooks",
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";

section {
  display: flex;

  .testo {
    width: 40%;

    i{
        color: $button
    }

    p{
        font-size: small;
        color: $grey-text;
    }

    .smol-title{
        font-size: smaller;
        text-transform: uppercase;
    }

    .big-title{
        font-size: 40px;
        color: $cards;

        span{
            color: $button;
        }
    }


  }

  .cover{
      text-align: center;
      width: 45%;

      img{
          width: 100%;
      }
  }

  .books {
    width: 60%;
    display: flex;
    gap: 30px;

    .prezzo {
      margin-top: 10px;
      font-size: x-large;
      color: $button;
      font-weight: bold;

      span {
        font-size: large;
      }
    }
  }

  button{
      margin-top: 30px;
  }
}
</style>