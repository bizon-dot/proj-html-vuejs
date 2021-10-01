<template>
  <section class="hero">
    
    <img src="../assets/img/artist-shape-01.png" class="orange shape"/>
  
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

      .hero{
        position:relative
        .shape{
          position:absolute;
        }
        .orange{
        //  display:none;
       //   color:orange;
          left: 100%;
        }
      }

</style>
