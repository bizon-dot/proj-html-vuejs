<template>
  <div class="container courses">
    <div class="header">
      <div class="handwriting">
        Artist coaching
      </div>
      <h1>
        Latest Online Course
      </h1>
      <div class="container-cards">
        <ul class="cards">
          <li v-for="(course,index) in courses" :key="index">
            <img class="img-fluid mb-3" :src="require(`@/${course.path}`)" :alt="course.title">
            <p class="price">{{course.price}} $</p>
            <p class="title">{{course.title}} $</p>
            <div class="info">
             <span>   <i class="far fa-calendar"></i> {{course.nLessons}} Lessons</span>
             <span> <i class="far fa-user"></i> {{course.students}} Students </span>
            </div>

          </li>

        </ul>

      </div>
    </div>


  </div>
</template>

<script>
  import courses from "../assets/data/data-courses.js";
  import Card from './Card.vue';

  export default {
    name: 'Courses',
    componets: {
      Card
    },
    data() {
      return {
        courses: courses,

      }
    },

  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";

  .courses {
    width: 80%;
    margin: 0 auto;

    .cards {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      li {
        list-style: none;
        flex-basis: 25%;

        img {

          height: 300px;
        }
      }
    }

  }
</style>