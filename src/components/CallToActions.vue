<template>
  <div class="call-to-action clearfix">
    <div class="col clearfix">
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
    <div class="col clearfix">
      <span>
        As a coach and mentor, my ultimate goal id yo motivate visual artists
        toward inspired action. I help you get you back on track to being the
        productive, creative, meaningful and authentic artist you truly want
        to be. I support artist in crafting and living a creative life as weel as
        feeling good about themselves and their art
      </span>
      <span>
        As an artist and an educator for nearly 30 years, I undestand what it
        takes to create,
      </span>

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

  /*   .col-left{
      float: left;
       .handwriting{
        font-size:2rem
    }
    }
    .col.right{
      float: left;
      margin: 0 auto;
      
    } */

  .col {
    float: left;
    width: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    > *{
      padding: em(10);
    }
  }

  .col > span {
    width:50%;
  }





  .title {
    margin-top: em(30);
    width: 50%;
  }
</style>