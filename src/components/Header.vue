<template>
  <header cclass="container">
    <div class="header-top">
      <label class="msg-timer">
        Starts TOMORROW! Our biggest event of the year
      </label>
      <label class="timer">
        <i class="far fa-clock"></i> 00 : 00 : 00
      </label>
      <button class="button bg-orange">Get ticket</button>
    </div>

    <div class="header-bottom">

      <div class="logo">
        <img src="../assets/img/dark-logo.png">
      </div>
      <div class="menu">
        <ul class="items">
          <li v-for="(link,index) in links" :key="index">
            <a> {{link.text.toUpperCase()}} </a>
          </li>
        </ul>

      </div>
      <div class="socials">
        <ul class="items">
          <li v-for="(icon,index) in socialIcons" :key="index">
            <img :src="require(`@/${icon.path}`)" :alt="icon.text" />
          </li>
        </ul>

      </div>

    </div>

  </header>
</template>

<script>
  import links from "../assets/data/link-nav.js";
  import socialIcons from "../assets/data/social-icons.js"
  export default {

    name: 'Header',
    data() {
      return {
        links: links,
        socialIcons: socialIcons,
      }
    }

  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "./style/general.scss";

  header{
    margin-bottom: em(20);
  }

  .header-top {
    min-height: 4em;
    line-height: 4em;
    background-color: #f5f5f5;
    display: flex;
    justify-content: center;
    align-items: baseline;
    gap: 20px;

    .msg-timer {
      color: $dusty-gray;
    }

    .timer {
      color: black;
      font-weight: 800;
    }
  }

  .header-bottom {
    min-height: 8em;
    line-height: 8em;
    display: flex;
    justify-content: space-around;
    align-items: baseline;

    .logo {
      height: em(100);
      width: em(300);

      img {
        width: 60%;
        height: auto;
      }
    }

    .menu,
    .socials {
      .items {
        list-style: none;
        display: flex;
        justify-content: space-between;

        li {
          padding: 0px 0.625em;
        }
      }
    }
  }
</style>