<template>
  <div id="app" >
   
    <Header/>
    <!-- <Hero /> -->
    <ServiceCoaching />
    <Testimonials />
    <Courses />
    <Events /> 
    <Blog />
    <CallToActions />
    <ContactMe />
    <Footer />
    <GoToTop />
      

     
  </div>
</template>

<script>
import Header from './components/Header.vue';
// import Hero from './components/Hero.vue';
import ServiceCoaching from './components/ServiceCoaching.vue';
import CallToActions from './components/CallToActions.vue';
import Testimonials from './components/Testimonials.vue';
import Courses from './components/Courses.vue';
import Blog from './components/Blog.vue';

import Events from './components/Events.vue';
import ContactMe from './components/ContactMe.vue'
import Footer from './components/Footer.vue';
import GoToTop from './components/GoToTop.vue';


export default {
  name: 'App',
  components: {
    Header,
 /*    Hero, */
    ServiceCoaching,
    CallToActions,
    Testimonials,
    Courses,
    Blog,
    Events,
    ContactMe,
    Footer,
    GoToTop
  },
  
}
</script>

<style lang="scss">
  @import "./style/general.scss";

#app {
  

  
  
  
  
}
</style>
