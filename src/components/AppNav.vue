<template>
  <nav class="d-flex justify-content-around">
      <img src="../assets/dark-logo.png" alt="">

      <div class="link">
          <p v-for="(item, index) in listaLink" :key="index"><a href="">{{item}}
          <i class="fa-solid fa-angle-down"></i></a></p>
      </div>

      <div class="media">
          <i class="fa-brands fa-twitter"></i>
          <i class="fa-brands fa-facebook-f"></i>
          <i class="fa-brands fa-instagram"></i>
          <i class="fa-brands fa-linkedin"></i>
      </div>
  </nav>
</template>

<script>
export default {
  name: 'AppNav',
  props: {
    
  },
  data(){
      return{
          listaLink: ['Home', 'Pages', 'Courses', 'Features', 'Blog', 'Shop']
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
nav{
    height: 50px;
    align-items: center;
}

img{
    height: 20px;
}

.link{
    height: 50px;
    display: flex;
    align-items: center;

    p{
        line-height: 50px;
        margin-bottom: 0;
    }
}

a{
    font-size: small;
    margin-right: 40px;

    i{
        font-size: smaller;
    }
}

i{
    margin-right: 20px;
}

</style>
