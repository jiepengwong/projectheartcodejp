<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> | 
    <router-link to="/about">About</router-link>
  </div> -->

  <Navbar />
  <LandingSection/>

</template>

<script>
  import Navbar from "@/components/NavBar.vue";
  import LandingSection from "@/components/LandingSection.vue"

  export default {
    components: {
      Navbar,
      LandingSection
    },

    data() {},

    methods: {
      scrollMeTo(refName) {
        var element = this.$refs[refName];
        var top = element.offsetTop;

        window.scrollTo(0, top);
      },
    },
  };
</script>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@100&display=swap");
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100&family=Playfair+Display&display=swap');

  * #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }

  #nav {
    padding: 30px;
  }

  #nav a {
    font-weight: bold;
    color: #2c3e50;
  }

  #nav a.router-link-exact-active {
    color: #42b983;
  }
</style>
