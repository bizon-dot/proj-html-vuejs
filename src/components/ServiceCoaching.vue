<template>

  <div class="service container">

    <div class="header">
      <p class="handwriting">Artist coaching </p>
      <h1>
        I undestand what it takes to create.
      </h1> 
      <h1>
        I can help you with
      </h1>
    </div>

    <div class="service-bottom">
      <div class="card">
        <div class="img-card">
          <img src="../assets/img/artist-box-image-01.png">

        </div>
        <div class="alt-card">
          <h3>Online courses</h3>
          <span> Online art coaching now offers you a very powerful way to redesign your artist mind </span>

        </div>
      </div>
      <div class="card">
        <div class="img-card">
          <img src="../assets/img/artist-box-image-02.png">

        </div>
        <div class="alt-card">
          <h3>One to One</h3>
          <span> Getting the necessary larity about the
            current state to help you improve your ability. </span>

        </div>

      </div>
      <div class="card">
        <div class="img-card">
          <img src="../assets/img/artist-box-image-03.png">

        </div>
        <div class="alt-card">
          <h3>Anywhere</h3>
          <span> Access to valuable and portable program
            which allow you to setup and live anywhere you want </span>

        </div>
      </div>
      <div class="card">
        <div class="img-card">
          <img src="../assets/img/artist-box-image-04.png">

        </div>
        <div class="alt-card">
          <h3>On time</h3>
          <span> Puctuality is our top priority because
            it's an essential criteria to assess a program quality </span>

        </div>

      </div>
    </div>
    <img src="../assets/img/maxcoach-shape-13.png" class="image-shape">

  </div>
</template>

<script>
  export default {
    name: 'service',

  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";

  .service {
    position: relative;
    
  }

  .image-shape {
    position: absolute;
    right: 0;
    top: em(200);

  }

  .service-top {
   
    * {
      padding: em(5);
    }

  }

  .service-bottom {
    padding: em(40);
    display: flex;
    justify-content: center;
    align-items: center;
    background-image: url("../assets/img/maxcoach-shape-14-1024x229.png");

    >*:first-child,
    >*:last-child {
      background-image: url("../assets/img/artist-shape-01-300x288.png");

    }

    .card {
      margin-left: em(5);

    }

    .alt-card {
      width: em(300);
    }

  }
</style>