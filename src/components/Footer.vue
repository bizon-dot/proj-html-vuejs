<template>
  <div class="footer">
    <!-- Footer Top -->
    <div class="footer-top">
      <!-- * Prima Colonna * Sezione Info * -->
      <div class="info">
        <h2>Address</h2>
        <p>{{info.address}}</p>
        <p>{{info.phone}} {{info.timetable}}</p>
        <p>{{info.email}}</p>
        <!-- Icone social -->
        <ul class="socialItems">
          <li v-for="(icon,index) in socialIcons" :key="index">
            <i :class="icon.ico"></i>
          </li>
        </ul>
      </div>
      <!-- * Seconda colonna * SiteMap -->
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
      <!-- * Terza colonna * Instagram Feed -->
      <div class="instagram-feed">
        <div class="header-social">
          <h2>Instagram</h2><label>@maxcoach</label>
        </div>
        <!-- Container Foto -->
        <div class="container-photos">
          <li v-for="(photo,index) in photosInstagram" :key="index">
            <img :src="require(`@/${photo.path}`)" :alt="photo.text" />
          </li>
        </div>
      </div>
    </div>
    <!-- Footer Bottom  -->
    <div class="footer-bottom">
      <i class="far fa-copyright"></i> {{currentYear}} Maxcoach. All Right Reserved
    </div>
  </div>
</template>

<script>
  // Importo i file con i dati (info + links) per il footer
  import * as data from "../assets/data/data-footer.js";
  // Icone social
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
        currentYear: "",
      }

    },
    // Funzione per ritornare l'anno corrente da usare nelcopyright
    created: function () {
      return this.currentYear = new Date().getFullYear();
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";

  .footer {
    color: $dusty-gray;
    padding: em(20);
  }

  .footer-top {
    display: flex;
    justify-content: space-between;
    font-weight: 400;
    .info > * {
      padding: em(10);
    }

    // Tolgo lo stile dalle liste
    .socialItems,
    .container-photos,
    .items {
      list-style: none;
      li {
        padding: em(10);
      }
    }

    .socialItems,
    .container-photos {
      display: flex;
    }

    .instagram-feed {
      .header-social {
        display: flex;
        flex-wrap: wrap;
        align-items: center;

        label {
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
    h2 {
      color: black;
    }
  }

  .footer-bottom {
    display: flex;
    align-items: center;
    justify-content: center;

  }
</style>