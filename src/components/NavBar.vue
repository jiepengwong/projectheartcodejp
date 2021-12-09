<template>
  <header id="navbar" class="sticky">

    <nav>



    <a href="#landing" class="logoname">Project Heartcode ❤️</a>
    <button @click="toggle()" class="hamburger"><fa class="text-white" icon="bars"></fa></button>
    <!-- <i class="fas fa-bars"></i> -->

      <ul id="nav-ul" class="nav-ul" >
        <!-- <a href="#landing">Home</a> -->
        <a href="#educate">Statistics</a>
        <a href="#tips">Tips</a>
        <a href="#helpline">Helpline</a>
        <a href="#inspiration">Stories</a>

      </ul>
    </nav>
  </header>
</template>

<script>
  export default {
    name: "Navbar",

    // created() {
    //   let initialScroll = this.getScrollPos();

    //   window.addEventListener("scroll", () => {
    //     var nav = document.querySelector("header");
    //     var isScrolling;
    //     window.clearTimeout(isScrolling);

    //     // Set a timeout to run after scrolling ends

    //     if (initialScroll > window.scrollY) {
    //       console.log("moving");
    //       nav.classList.add("nav--hidden");
    //     }

    //     if (initialScroll < window.scrollY) {
    //       console.log("moving");
    //       nav.classList.add("nav--hidden");
    //     } else if (initialScroll == window.scrollY == 0) {
    //       nav.classList.remove("nav--hidden");
    //     }

    //     isScrolling = setTimeout(function () {
    //       // Run the callback
    //       console.log("Scrolling has stopped.");
    //       nav.classList.remove("nav--hidden");
    //     }, 500);

    //     // else  {
    //     //   console.log("up")
    //     //   nav.classList.remove("nav--hidden")

    //     // }

    //     initialScroll = window.scrollY;
    //   });
    // },

    methods: {
      getScrollPos() {
        let lastScrollY = window.scrollY;
        return lastScrollY;
      },

      toggle() {
        const navUL = document.getElementById('nav-ul');
        navUL.classList.toggle('show');
        console.log("cick")

      }
    },
  };
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    background-color: #24252a;
  }

  header{
    z-index: 999;
     z-index: 999;
    transition: transform 0.2s;
    color: white;
  }

  .logoname{
    text-decoration: none;
    color: rgb(255, 255, 255);
    font-weight: bolder;
    font-family: 'VT323', monospace;
    font-size: 20px;
    padding-left: 10px;
  }

  nav {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    padding: 15px;
   
  }

  /* li,
  a {
    font-family: "Montserrat", sans-serif;
    font-weight: bolder;
    font-size: 16px;
    color: white;
    text-decoration: none;
  } */

  .nav-ul {
    display: flex;
    align-items: center;
    justify-content: center;
    /* padding: 0; */
    list-style-type: none;
  }

  .nav-ul a{
    display: inline-block;
    padding: 10px 20px;
    text-decoration: none;
    color: white;
  }

  a:hover {
  color:#00c2cb;
}

  .hamburger{
    border: 0;
    font-size: 20px;
    display: none;
    cursor: pointer;

  }

  .hamburger:focus-visible{
    outline: none;
  }
  .sticky {
    position: -webkit-sticky;
    position: sticky;
    top: 0;
  }
  .nav--hidden {
    transform: translateY(calc(-86px));
    transition: transform 0.2s;

    box-shadow: none;
  }

  @media screen and (max-width: 700px){

    

    .nav-ul {
      display: none;
      flex-direction: column;
      width: 100%;
    }
     .show {
      display:flex !important;
    }

   

    .hamburger {
      display: block;
    }

  }
</style>
