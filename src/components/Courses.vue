<template>
  <div class="container courses">
    <div class="header">
      <div class="handwriting">
        Artist coaching
      </div>
      <h1>
        Latest Online Course
      </h1>
    </div>
      <div class="container-cards">
        <ul class="cards">
          <li v-for="(course,index) in courses" :key="index">
            <div class="card">
              <img class="img-fluid mb-3" :src="require(`@/${course.path}`)" :alt="course.title">
              <div class="info">
              <p class="price">{{course.price}}.00 $</p>
              <p class="title">{{course.title}} </p>
              
                <span> <i class="far fa-calendar"></i> {{course.nLessons}} Lessons</span>
                <span> <i class="far fa-user"></i> {{course.students}} Students </span>
              </div>

            </div>
          </li>

        </ul>

      </div>
    </div>
</template>

<script>
  import courses from "../assets/data/data-courses.js";
  export default {
    name: 'Courses',
    
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
 
    .card{
      > *{
     padding:20px;
    }
    .price{
      color:#ef6f31;
      font-weight: 800;
      font-size:1rem;
    }
    .title{
      font-size: 1.5rem;
      font-weight: bolder;
      color: black;
      text-transform: capitalize ;
    }
    }

    .card:hover{
              box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
        .info{
          border: solid 2px orange;
          margin-top: -20px;
        }

    }
   
    .cards {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
     
      .info {
        color:gray;
        span {
          padding: em(5);
        }
      }
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