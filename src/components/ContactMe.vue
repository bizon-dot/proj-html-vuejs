<template>
<div class="contact">
  <!-- <div class="container"> -->
    <div class="row">
      <div class="col">
         <img class="photo-right" src="../assets/img/artist-shape-color-paint-top-left-300x170.png"  />
      </div>
    
      <div class="col">
          <h2 class="title">Newsletter to get in touch </h2>
      </div>
      <div class="col">
        <input type="email" id="email" placeholder="Your email"
       pattern=".+@globex\.com" size="30" required>

      </div>
      <div class="col" >
         <img src="../assets/img/artist-shape-color-paint-bottom-right-300x153.png"  />
      </div>
    </div>
      
  

  </div>
  
</template>

<script>
export default {
  name: 'ContactMe',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";
  .photo-right{
    height: 64%;
    width: auto;
  }

.row{
   display: flex;
   flex-direction: row;
   //justify-content: flex-start;
   
   .col{
     line-height: 153px;  
     text-align: center;
     flex: 25%;

     .title{
       color: white;
       font-size: 25px;
       font-weight: bolder;
     }

     input[type=email] {
        border: none;
        border-bottom: 2px solid white;
        outline: 0 none;
        background-color: $dark-vibrant;
        
      }
      ::placeholder{
          color:white;
          font-size:20px;
        }
   }
}

.contact{
  background-color: $dark-vibrant;
  max-height: 153px;
}

</style>
