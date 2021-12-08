<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> | 
    <router-link to="/about">About</router-link>
  </div> -->

  <Navbar />
  <section id="landing">
  <LandingSection/>
  </section>
  <section id="educate">
    <Statistics/>
  </section>

  <section id="symptoms">
    <Symptoms/>
  </section>

  <section id="tips">
    <Tips/>
  </section>

  <section id="helpline">
    <HelpLine/>
  </section>

</template>

<script>
  import Navbar from "@/components/NavBar.vue";
  import LandingSection from "@/components/LandingSection.vue"
  import Statistics from "@/components/Statistics.vue"
  import Symptoms from "@/components/Symptoms.vue"
  import Tips from "@/components/Tips.vue"
  import HelpLine from "@/components/Helpline.vue"





  export default {
    components: {
      Navbar,
      LandingSection,
      Statistics,
      Symptoms,
      Tips,
      HelpLine
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
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100&family=Oswald:wght@200&family=Playfair+Display&display=swap');

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
    color: #36ebff;
  }
  #educate{
    background: #e4faff;
  }

   .highlight {
    color: #00c2cb;
  }

  #tips{
    background:  #ffe6cd;
  }
</style>
