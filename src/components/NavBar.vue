<template>
  <header id="navbar" class="sticky">
    <!-- <a href="#landing"><img src="" alt="logo" /></a> -->

    <nav>
      <ul class="nav-link">
        <a href="#landing">Home</a>
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

    created() {
      let initialScroll = this.getScrollPos();

      window.addEventListener("scroll", () => {
        var nav = document.querySelector("header");
        var isScrolling;
        window.clearTimeout(isScrolling);

        // Set a timeout to run after scrolling ends

        if (initialScroll > window.scrollY) {
          console.log("moving");
          nav.classList.add("nav--hidden");
        }

        if (initialScroll < window.scrollY) {
          console.log("moving");
          nav.classList.add("nav--hidden");
        } else if (initialScroll == window.scrollY == 0) {
          nav.classList.remove("nav--hidden");
        }

        isScrolling = setTimeout(function () {
          // Run the callback
          console.log("Scrolling has stopped.");
          nav.classList.remove("nav--hidden");
        }, 500);

        // else  {
        //   console.log("up")
        //   nav.classList.remove("nav--hidden")

        // }

        initialScroll = window.scrollY;
      });
    },

    methods: {
      getScrollPos() {
        let lastScrollY = window.scrollY;
        return lastScrollY;
      },
    },
  };
</script>

<style scoped>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    background-color: #24252a;
  }

  header {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 30px 10%;
    z-index: 999;
    transition: transform 0.2s;
  }

  li,
  a {
    font-family: "Montserrat", sans-serif;
    font-weight: bolder;
    font-size: 16px;
    color: white;
    text-decoration: none;
  }

  .nav-link {
    list-style: none;
  }

  .nav-link a {
    display: inline-block;
    padding: 0px 20px;
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
</style>
