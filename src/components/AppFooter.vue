<template>
  <footer>
    <section>
      <div class="left">
        <p class="bold">Adress</p>
        <p>382 NE 191st St # 87394 Miani, FL 33179-3899</p>
        <p>+1(305) 547-9909 (9am - 5pm EST, Monday - Friday)</p>
        <p>support@maxcoach.com</p>
        <p>
          <i class="fa-brands fa-twitter"></i>
          <i class="fa-brands fa-facebook-f"></i>
          <i class="fa-brands fa-instagram"></i>
          <i class="fa-brands fa-linkedin"></i>
        </p>
      </div>

      <div class="right">
          <ul>
              <li><a href="" class="bold">Explore</a></li>
              <li><a href="">Start Here</a></li>
              <li><a href="">Blog</a></li>
              <li><a href="">About</a></li>
          </ul>
          <ul>
              <li class="color-diff">haha</li>
              <li><a href="">Success Story</a></li>
              <li><a href="">Courses</a></li>
              <li><a href="">Contact us</a></li>
          </ul>
          <ul>
              <li><a href="" class="bold">Information</a></li>
              <li><a href="">Membership</a></li>
              <li><a href="">Purchase Guide</a></li>
              <li><a href="">Privacy policy</a></li>
              <li><a href="">Terms of Service</a></li>
          </ul>
      </div>
    </section>
    <p class="middle">	&copy;2020 Maxcoach, All Rights Reserved</p>

    <i class="fa-solid fa-arrow-up-long"></i>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';

footer{
    padding-top: 30px;
    padding-bottom: 30px;
    background-color: $footer;
    color: $grey-text;
    font-size: small;
    position: relative;

    i{
        margin-right: 30px;
        font-size: medium;
    }

    .bold{
        font-weight: bold;
        color: white;
    }

    a{  
        color: $grey-text;
        font-size: small;
    }

    ul{
        list-style-type: none;

        li{
            margin-bottom: 10px;
        }

        .color-diff{
            color: $footer;
        }
    }

    .middle{
        text-align: center;
    }

    .right{
        display: flex;
    }

    section{
        display: flex;
        justify-content: space-around;
    }

    .fa-arrow-up-long{
        position: absolute;
        bottom: 30px;
        right: 10px;
        width: 50px;
        height: 50px;
        border-radius: 50%;
        color: white;
        font-size: 20px;
        text-align: center;
        line-height: 50px;
        background-color: $button;
    }

}
</style>