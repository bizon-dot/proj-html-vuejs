<template>
  <div class="container testimonials">
    <div class="video">
            <img class="z-999" src="../assets/img/artist-video-poster.jpg">
            <img class="centered z-999" src="../assets/img/icon-youtube-play.png">
            <img class="bottom-right" src="../assets/img/maxcoach-shape-12-150x150.png">
            <img class="top-left" src="../assets/img/maxcoach-shape-05-150x150.png">
    </div>

    <div class="feedbacks">
    <div class="header">
      <div class="handwriting">
        Testimonials
      </div>
      <h1>
        Why do people love me?
      </h1>
    </div>
    <div class="container-cards">
      <ul class="cards">
        <li v-for="(testimonial,index) in testimonials" :key="index">
          <div class="card">
            <p class="title">
              {{testimonial.title}}
            </p>
            <p class="text">
              {{testimonial.text}}
            </p>
            <div class="box-author">
              <div class="box-img">
                <img class="img-fluid mb-3" :src="require(`@/${testimonial.path}`)" :alt="testimonial.author">
              </div>
              <div class="box-info">
                <p class="author">
                  {{testimonial.author}}
                </p>
                <p class="job">
                 / {{testimonial.job}}
                </p>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
    <div class="box-dots">
      <i class="fas fa-circle"></i>
      <i class="fas fa-circle"></i>
      <i class="fas fa-circle"></i>

    </div>
  </div>
  </div>
</template>

<script>
  import testimonials from "../assets/data/data-testimonials.js";

  export default {
    name: 'Testimonials',

    data() {
      return {
        testimonials: testimonials,
      }
    }

  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";

  .video{
    display: flex;
    align-items: center;
    justify-content: center;
    position:relative;

  

  }

  .testimonials {
       background-image: url("../assets/img/artist-shape-01-600x577.png");
       
    
    .cards {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      margin: em(20) em(20);

      .card {
        min-height: 300px;
        width: auto;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
        transition: 0.3s;
        margin: 5px;
        padding: 10px;
        background-color: whitesmoke;
      }

      .card:hover {
        box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);

        .text,
        .title,
        .author,
        .job {
          color: black;
        }
      }

      .title {
        font-size: 1rem;
        font-weight: bolder;
        padding: 2em;
      }

      .text,
      .title,
      .author,
      .job {
        color: $silver;
      }

      li {
        list-style: none;
      }

      .box-author {
        display: flex;
        flex-direction: row;
        padding: 10px;

        .box-img {
          margin-right: 15px;

          img {
            border-radius: 50%;
            width: 70px;
            height: 70px;
          }
        }

        .box-info {
          .author,
          .job {
            text-transform: capitalize;
          }
        }
      }
    }

    // first-of-type first-of-child non riesco a colorare il primo pallino

    .box-dots {
      display: flex;
      justify-content: center;
      color:gray;
      
      *{
        margin-left: em(30);
       
      }
    }

  
    
  }
</style>