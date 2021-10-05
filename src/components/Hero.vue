<template>
  <section class="hero">
     <div class="header-hero centered">
      <div class="handwriting">
        Hello, Im Matin
      </div>
      <h1>
        Artist Coaching And Mentoring 
        Might Be For You.
      </h1>
      <button class="button bg-orange">Get started today</button>
    </div>

    <div class="left">
      <img src="../assets/img/artist-hero-image-01.jpg" class="b-l"/>
      <img src="../assets/img/artist-hero-image-02-232x300.jpg" class="t-r"/>
      <img src="../assets/img/artist-hero-image-03-204x300.png" class="b-r"/>
      <img src="../assets/img/artist-shape-03-201x300.png" class="h-80"/>




    </div>
    
    <div class="right">
      <img src="../assets/img/artist-hero-image-04.jpg" class="b-right z-999"/>
      <img src="../assets/img/artist-shape-01-600x577.png" class="h-90 b-right "/>
      <img src="../assets/img/artist-shape-04-127x300.png" class=" t-right "/>
      <img src="../assets/img/artist-shape-05.png" class="b-b-right"/>
      <img src="../assets/img/maxcoach-shape-12-96x96.png" class="b-left"/>


    </div>  
  </section>
</template>

<script>
export default {
  name: 'Hero',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";


      .hero{
        position:relative;
        height: em(500);
        width: 100%;
        background-color: lighten($hint-of-red, 2%);

      .header-hero{
        display: flex; 
        flex-direction: column;
        align-items: center;
        

        button{
          height: 50px;
          width:150px;
        }
        
        .handwriting{
          font-size: 50px;
          padding: 10px;
        }

        h1{
          padding:10px;
        }
      }

      .h-90{
        height: 90%;
      }

      .b-right{
        position:absolute;
        bottom: 2%;
        right: 10%; 
      }

      .b-b-right{
        position: absolute;
        bottom:0;
        right:2%;
      }

      .t-right{
        position:absolute;
        bottom: 40%;
        right: 8%;
      }

      .b-left{
        position:absolute;
        bottom: 0;
        left:75%;
      }
      }

      .b-l{
        position: absolute;
        bottom: 10%;
        left: 5%;
        z-index:200;
      }

      .t-r{
        position:absolute;
        bottom: 35%;
        left: 12%;
        z-index:190;

      }

      .b-r{
        position:absolute;
        bottom:10%;
        left:20%;
      }

      .h-80{
        position: absolute;
        top:20%;
        height:em(400);
        width: 20%;
      }
</style>
