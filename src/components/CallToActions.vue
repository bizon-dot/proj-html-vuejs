<template>
  <div class="container row">
    <div class="col">
      <img src="../assets/img/artist-quote-icon.png">
      <div class="title">
        <h1>I coach and mentor
          visual artists, like
          you, to Create Like
          You Mean It
        </h1>

      </div>
      <div class="handwriting">
        Martin Glarrix
      </div>

    </div>
    <div class="col">
      <p class="justify p-4">
        As a coach and mentor, my ultimate goal id yo motivate visual artists
        toward inspired action. I help you get you back on track to being the
        productive, creative, meaningful and authentic artist you truly want
        to be. I support artist in crafting and living a creative life as weel as
        feeling good about themselves and their art
      </p>
      <p class="justify p-4">
        As an artist and an educator for nearly 30 years, I undestand what it
        takes to create.
      </p>
      <button class="button bg-light-orange">Get ticket</button>

    </div>

  </div>
</template>

<script>
  export default {
    name: 'CallToAction',
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";

  .row {
    display: flex;
    width: 80%;
    margin: 0 auto;
    margin-bottom: em(40);

   
  }

  .col {
    flex: 50%;
    text-align: center;
    padding: 30px;


    .title {
      padding: 20px;
    }

    .justify{
      margin-bottom: em(15);
    }

    

    
  }
</style>