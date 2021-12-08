<template>
  <h1 class="py-5">
    <b>How <span class="highlight">YOU</span> can help people with mental
    conditions</b>
  </h1>

  <div class="container">
    <div class="row">



        
      <div class="col-sm-6 order-lg-1 order-2">
        <p class="text-start">
          Research confirms that support from family and friends is a key part
          of helping someone who is going through a mental illness. This support
          provides a network of practical and emotional help. These are some
          ways where you can extend your help to them
        </p>

        <div class="text-start pt-3" v-for="tip in tips" :key="tip">
            <h4><b>{{tip.title}}</b></h4>

            <p>{{tip.description}}</p>

        </div>

        <!-- <ul>
          <li>Be a listening ear to them
              <p>Just being there for them would be able to comfort them alot</p>
          </li>
          <li>Be empathetic towards them
              <p>It is important to understand their condition. </p>
          </li>
          
          <li>Be patient
              <p>It may be particularly hard for such people to express themselves freely. Extra patience will be needed for us to understand them effectively</p>
          </li>
        </ul> -->
      </div>


      <div class="order-sm-last col-sm-6 order-lg-2 order-1">
        <img
        class="pb-4 img-fluid"
        
        src="../assets/helping.png">
      </div>

    </div>

  </div>
</template>

<script>
  export default {
    name: "Tips",

    data() {
      return {
          tips: [
          {
            title: "Be their listening ear",
            description:
              "Just being there for them would be able to comfort them alot. This would make them feel more reassured and more comforted and they would more tempted to open up even more",
            
          },
          {
            title: "Be Empathetic",
            description:
              "The first way to diffuse a tense situation is to establish rapport with the person in distress. Listening quietly, without engaging in problem-solving, signals that you are on that person’s side.",
           
          },
          {
            title: "Be Patient",
            description:
              "Sometimes, it may be hard for people facing mental illnesses to open up. Patient is key as we do not want to push and disregard their thoughts and feelings.",
            
          },
        ],

      };
    },
  };
</script>

<style scoped>
*{
    font-family: "Playfair Display", serif;

}
</style>
