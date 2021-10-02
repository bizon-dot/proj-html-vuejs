<template>
  <div id="app" >
   
    <Header/>
    <!-- <Hero /> -->
    <ServiceCoaching />
    <CallToActions />


     <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
// import Hero from './components/Hero.vue';
import ServiceCoaching from './components/ServiceCoaching.vue';
import CallToActions from './components/CallToActions.vue';
import Footer from './components/Footer.vue';


export default {
  name: 'App',
  components: {
    Header,
 /*    Hero, */
    ServiceCoaching,
    CallToActions,
    Footer
  }
}
</script>

<style lang="scss">
  @import "./style/general.scss";

#app {
  
}
</style>
