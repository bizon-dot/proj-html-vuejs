<template>
  <div id="app" >
   
    <Header/>
    <!-- <Hero /> -->
    <ServiceCoaching />
    <Testimonials />
    <Courses />
    <CallToActions />


     <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
// import Hero from './components/Hero.vue';
import ServiceCoaching from './components/ServiceCoaching.vue';
import CallToActions from './components/CallToActions.vue';
import Testimonials from './components/Testimonials.vue';

import Courses from './components/Courses.vue';

import Footer from './components/Footer.vue';


export default {
  name: 'App',
  components: {
    Header,
 /*    Hero, */
    ServiceCoaching,
    CallToActions,
    Testimonials,
    Courses,
    Footer
  }
}
</script>

<style lang="scss">
  @import "./style/general.scss";

#app {

  
  
  
  
}
</style>
