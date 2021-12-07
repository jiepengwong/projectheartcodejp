<template>
  <header class="landingheader">
    <div class="container">
      <div
        class="row mt-5 h-100 align-items-center text-white justify-content-center text-center"
      >
        <div class="col-lg-10 align-self-end">
          <h1 class="mt-5 font-weight-bold text-uppercase">
            <b>You are <span class="highlight">not </span>alone.</b>
          </h1>
          <hr
            style="border-color: #119ddd; border-width: 0.25rem"
            class="divider"
          />
        </div>

        <div class="col-lg-8 align-self-baseline text-center">
          <h3 class="mb-5" >Mental illness is a real issue and we need to normalise this</h3>

          <a class="btn btn-xl text-white">Find out more</a>
        </div>

      </div>
    </div>
  </header>
</template>

<script>
  export default {
    name: "LandingSection",

    data() {},

    methods: {},
  };
</script>

<style scoped>
  header.landingheader {
    padding-top: 10rem;
    padding-bottom: calc(10rem - 72px);
    background-image: url(../assets/landingpage.png);
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: scroll;
    background-size: cover;
    height: 100vh;
    font-family: "Playfair Display", serif;
  }

  h1 {
    font-size: 3.5rem;
  }

  hr.divider {
    border-width: 0.25rem;
    color: #00c2cb !important;
    height: 4px;
    opacity: 100;
  }

  .highlight {
    color: #00c2cb;
  }

  .h-100 {
    height: 100% !important;
  }
    .btn{
    border-radius: 50%;;
    }

    .align-self-baseline {
    align-self: center !important;
    
    }

    .btn-xl {
    padding: 1.25rem 2.25rem;
    font-size: 0.85rem;
    font-weight: 700;
    text-transform: uppercase;
    border: none;
    background: #00c2cb;
    border-radius: 29rem;
    margin:0 auto;
    text-align: center;
    opacity: 0.6;
    transition: 0.3s;
}

.btn-xl:hover {opacity: 1}
</style>
