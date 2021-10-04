<template>
<div class="contact">
  <div class="container">
    <div class="row">
      <div class="col">
          <h2>Newsletter to get in touch </h2>
      </div>
      <div class="col">
        <input type="email" id="email" placeholder="Your email"
       pattern=".+@globex\.com" size="30" required>

      </div>
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

.row{
   display: flex;
   flex-direction: row;
   
   .col{
     line-height: 200px;  
     text-align: center;
     flex: 50%;
   }
}

.contact{
  background-color: $dark-vibrant;
  min-height: 200px;
}

</style>
