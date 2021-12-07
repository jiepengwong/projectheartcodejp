<template>
  <header>
    <img src="" alt="logo" />

    <nav>
      <ul class="nav-link">
        <a href="/">Home</a>
        <a href="/">Home</a>
        <a href="/">Home</a>
        <a href="/">Home</a>
        <a href="/">Home</a>

       
      </ul>
    </nav>
  </header>
</template>

<script>
  export default {
    name: "Navbar",
  };
</script>

<style scoped>
  @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@100&display=swap");

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    background-color: #24252a;
  }

  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 30px 10%;
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
</style>
