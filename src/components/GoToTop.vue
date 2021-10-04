<template>
  <div class="go-to-top">
           <button id="goToTop" @click="goToTop()"><i class="fas fa-arrow-up"></i></button> 
  </div>
</template>

<script>
export default {
  name: 'GoToTop',
  methods: {
    goToTop(){
          document.documentElement.scrollTop = 0;       
    }
  }
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";

 #goToTop {
  display: block;
  position: fixed; 
  bottom: 20px; 
  right: 30px; 
  z-index: 99; 
  border: none;
  outline: none; 
  background-color: darken($tulip, 2%);
  color: white; 
  cursor: pointer; 
  padding: em(5); 
  height: em(50);
  width: em(50);
  border-radius: 50%; 
  font-size: em(18); 
}

</style>
