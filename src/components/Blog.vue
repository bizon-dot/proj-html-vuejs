<template>
<div class="blog">
  <div class="container ">
    <div class="header">
      <div class="handwriting">
        Articles and tips
      </div>
      <h1>
        Latest From Blog
      </h1>
    </div>
    <div class="container-blog">
      <!-- Card Post -->
      <ul class="cards">
        <li v-for="(post,index) in posts" 
            :key="index">
          
           <div class="card" v-if="!(index==1)">
            <div class="box-image">
                <img class="img-fluid mb-3" :src="require(`@/${post.path}`)" :alt="post.title">
            </div>
            <div class="category"> 
                  {{post.category}}
            </div>
            <div class="title"> 
                  {{post.title}}
            </div>
            <div class="box-info">
                <i class="far fa-calendar"></i>  {{post.date}}
                <i class="far fa-eye"></i>   {{post.views}}
             </div>
         </div>

          <!-- Central Card Post -->
          <div v-else class="card-bg">
             <div class="box-info">
                <i class="far fa-calendar"></i>  {{post.date}}
                <i class="far fa-eye"></i>   {{post.views}}
             </div>
            <div class="title"> 
              {{post.title}}
            </div>
            <div class="category">
               {{post.category}}
            </div>
          </div>
        </li>
      </ul>
    </div>
    <div class="row">

      <span>Get into details now? </span><a> View all posts <i class="fas fa-arrow-right"></i></a>

    </div>
  </div>
</div>
</template>

<script>
  import posts from "../assets/data/data-blog.js";

  export default {
    name: 'Blog',
    data() {
      return {
        posts: posts

      }
    }

  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";

  .blog{
    background-image: url("../assets/img/maxcoach-shape-14-1536x343.png");
    margin-bottom: 70px;
  }

  .cards {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    
    li {
      list-style: none;
    }
  }

  .card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    width: 300px;
    height: 350px;
    padding: 20px;
    
    
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);

    .category {
      text-transform: uppercase;
      color: $silver;
      font-weight: 500;
    }

    .title,
    .category,
    .box-info{
      padding: 10px;
    }

    .box-info{
      color: $silver;
    }

    .title {
      text-transform: capitalize;
      font-size: 16px;
      font-weight: bolder;
      
    }

    .box-image {
      height: 150px;
      width: 250px;

      img {
        height: 90%;
        width: 100%;
      }
    }

   
  }
   

  .card-bg {
    height: 680px;
    width: 500px;
    background-image: url("../assets/img/artist-blog-02-500x680.jpg");
    display: flex;
    flex-direction: column-reverse;
    align-content: flex-end;
    .title{
      text-transform: capitalize;
      font-size: 30px;
      font-weight: 900;
      padding:10px;
      color:white;
    }
    .category{
      color:white;
      text-transform: uppercase;
      padding:10px;

    }

    .box-info{
      padding: 10px;
      color:white;
    }
  }

  .row{
    display:flex;
    margin-top: 30px;
    align-content: center;
    justify-content: center;
    span{
        color:$silver;
        font-weight: bolder;
    }
    a{
      color:#ef6f31;
      margin-left:10px;
      text-decoration: underline;
    }
  }
</style>