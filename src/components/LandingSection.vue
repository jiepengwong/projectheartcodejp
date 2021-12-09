<template>
  <header class="landingheader">
    <div class="container">
      <div
        class="row mt-5 h-100 align-items-center text-white justify-content-center text-center"
      >
        <div class="col-lg-12">
          <h1 class="mt-5 font-weight-bold text-uppercase">
            <b>You are <span class="highlight">not </span>alone.</b>
          </h1>
          <hr
            style="border-color: #119ddd; border-width: 0.25rem"
            class="divider"
          />
        </div>

         <div class="row">
          
        </div>

        <div class="col-lg-12 text-center">
          <h3 class="mb-5">
            Mental illness is a real issue and we need to normalise this
          </h3>



          <div class="row">
          <div class="col-md-3 "></div>
          <div class="col-md-3 ">
            <a href="#educate" class="btn btn-xl text-white mobile">Find out more</a>
          </div>
          <div class="col-md-3">
            <a href="#helpline" class="btn btn-xl text-white mobile">Seek Help Now</a>
          </div>
          <div class="col-md-3 "></div>
        </div>
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

  .h-100 {
    height: 100% !important;
  }
  .btn {
    border-radius: 50%;
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
    margin: 0 auto;
    text-align: center;
    opacity: 0.6;
    transition: 0.3s;
  }

  .btn-xl:hover {
    opacity: 1;
  }


  @media screen and (max-width: 700px){
    .mobile{
      display: none;
    }
  }
</style>
