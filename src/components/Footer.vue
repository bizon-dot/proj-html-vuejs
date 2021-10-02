<template>
  <div class="footer-top">
    <div class="info">
      <h2>Address</h2>
      <p>{{info.address}}</p>
      <p>{{info.phone}} {{info.timetable}}</p>
      <p>{{info.email}}</p>

      <ul class="socialItems">
        <li v-for="(icon,index) in socialIcons" :key="index">
          <img :src="require(`@/${icon.path}`)" :alt="icon.text" />
        </li>
      </ul>

    </div>


    <div class="linksExplore">
      <h2>Explore</h2>
      <ul class="items">
        <li v-for="(link,index) in linksExplore" :key="index">
          <a> {{link.text}} </a>
        </li>
      </ul>

    </div>

    <div class="linksInformation">

      <h2>Information</h2>
      <ul class="items">
        <li v-for="(link,index) in linksInformation" :key="index">
          <a> {{link.text}} </a>
        </li>
      </ul>

    </div>

    <div class="social">
      <div class="headerr">
        <h2>Instagram</h2><label>@maxcoach</label>
      </div>

      <div class="container-photos">
        <li v-for="(photo,index) in photosInstagram" :key="index">
          <img :src="require(`@/${photo.path}`)" :alt="photo.text" />
        </li>
      </div>


    </div>

  </div>
</template>

<script>
  import * as data from "../assets/data/data-footer.js";
  import socialIcons from "../assets/data/social-icons.js";
  export default {
    name: 'Footer',

    data() {
      return {
        linksExplore: data.linksExplore,
        linksInformation: data.linksInformation,
        info: data.info,
        socialIcons: socialIcons,
        photosInstagram: data.photosInstagram,
      }

    },



  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";

  .footer-top {
    display: flex;
    justify-content: space-between;
    width: 80%;
    margin: 0 auto;
    color: $dusty-gray;
    font-weight: 400;
    .info > *{
      padding: em(10);
    }
    .socialItems,
    .container-photos, 
    .items{
      list-style: none;
       li {
        padding: em(10);

      }
    }
    
    .socialItems,
    .container-photos {
      display: flex;
    }

    .social {
      .headerr {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        label{
          margin-left: em(5);
          color: #ef6f31;
        }
        
      }
    }

    .container-photos {

      img {
        height: em(150);
        width: em(150);
        object-fit: cover;
      }
    }

    h2{
      color:black;
    }
  }
</style>