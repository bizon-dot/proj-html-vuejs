<template>
  <div class="container testimonials">
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
            <p class="title">{{testimonial.title}} </p>
            <p class="text">{{testimonial.text}} </p>
            <div class="box-author">
              <img class="img-fluid mb-3" :src="require(`@/${testimonial.path}`)" :alt="testimonial.author">
              <p class="author">{{testimonial.author}} </p>
              <p class="job">{{testimonial.job}} </p>
            </div>


            <!--  <img class="img-fluid mb-3" :src="require(`@/${course.path}`)" :alt="course.title">
              <p class="price">{{course.price}}.00 $</p>
              <p class="title">{{course.title}} </p> -->
            <!-- {{testimonial}} -->
          </div>
        </li>

      </ul>

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
  .testimonials {
     width: 80%;
    margin: 0 auto;
    .cards {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;

      li{
        list-style: none;
      }
    }

    .card {
      background-color: whitesmoke;
    }

    // background-image: url("/assets/image/artist-shape-01-600x577.png");
  }
</style>