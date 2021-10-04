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
            <!-- <div v-bind:class="{ active: isActive }"></div> -->
            <div class="row" :class="(index > 1) ? 'margin' : 'null' " >
              <div class="col img">
                   <img class="img-fluid mb-3" :src="require(`@/${event.path}`)" :alt="event.title">
              </div>
               <div class="col">
                 <p class="date"> {{event.date}} </p>
                 <p class="title"> {{event.title}} </p>
                 <p class="location"><i class="fas fa-map-marker-alt"></i> {{event.location}} </p>
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
 @import "./style/general.scss";


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
    .date{
      color:$silver;
      text-transform: uppercase;
      font-weight: 500;
      padding:10px;
    }
    .title{
      font-size:16px;
      font-weight: bolder;
      text-transform: capitalize;
      padding:10px;
    }

    .location{
      color:$silver;
      text-transform: capitalize;
      font-weight: 500;
      padding: 10px;
    }
  }

  
}

.margin{
    margin-left: 280px;
  }

</style>
