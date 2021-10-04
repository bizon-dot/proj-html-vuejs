<template>
  <div class="container events">
     <div class="header">
      <div class="handwriting">
        Upcoming events
      </div>
      <h1>
        Let's work together
      </h1>
    </div>
     <div class="container-cards">
        <ul class="cards">
          <li v-for="(event,index) in events" :key="index">
            <div class="row">
              <div class="col img">
                   <img class="img-fluid mb-3" :src="require(`@/${event.path}`)" :alt="event.title">
              </div>
               <div class="col">
                 <p> {{event.date}} </p>
                 <p> {{event.title}} </p>
                 <p> {{event.location}} </p>
              </div>
              
           
            </div>
          </li>

        </ul>

      </div>
    
  </div>
</template>

<script>
import events from "../assets/data/data-events.js";

export default {
  name: 'Events',
  data(){
    return{
      events:events,
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.container-cards{
  .cards{
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
  }
  li{
    list-style: none;
    flex-basis: 50%;
  }
}
.row{
  display: flex;
  justify-content: center;
  align-items: center;
  
  .col{
    flex:50%;
  }
}

</style>
