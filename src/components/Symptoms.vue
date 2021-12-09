<template>
  <h1 class="py-5 "><b>Common Symptoms Of Mental Illnesses</b></h1>

<font-awesome-icon icon="user-secret" />

  <div class="cards-wrapper py-4">
    <div
      class="service card-effect col-sm-5 col-lg-2"
      :key="card.title"
      v-for="card of cards"
    >
      <h4 class="service-card-title "><u>{{ card.title }}</u></h4>
      <img
        class="my-4 service-img"
        :src="require(`../assets/${card.imageSrc}.png`)"
      />
      <p class="service-card-desc">
        {{ card.description }}
      </p>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Symptoms",

    data() {
      return {
        cards: [
          {
            title: "Sadness",
            description:
              "People with existing mental conditions often experience a feeling of sadness and loss of interest, which stops them doing your normal activities.",
            image: "../assets/sadness.png",
            imageSrc: "sadness",
          },
          {
            title: "Withdrawal/Loneliness",
            description:
              "They tend to avoid people or have any form of interaction, and they are often seculded in their own space",
            image: "../assets/sadness.png",
            imageSrc: "loneliness",
            link: "/image",
          },
          {
            title: "Anger",
            description:
              "People with mental illnesses tend to have mood spikes and demonstrate aggressive tendency to other people",
            image: "../assets/sadness.png",
            imageSrc: "swear",

            link: "/charts",
          },
          {
            title: "Fatigueness",
            description:
              "People who are suffering from mental illnesses often have sleep problems. They may sleep too much or not sleep at all.",
            image: "../assets/sadness.png",
            imageSrc: "fatigue",
          },
        ],
      };
    },
  };
</script>

<style scoped>
 * {
    /* color: white; */
    font-family: "Playfair Display", serif;
    
  }
  .cards-wrapper {
    display: flex;
    flex-wrap: wrap;
    /* flex-direction: column; */
    gap: 1rem 2rem;
    justify-content: center;
    margin-top: 1rem;
  }

  .card-effect {
    transition: all 0.35s ease;
    /* transition-property: all;
        transition-duration: 0.35s;
        transition-timing-function: ease;
        transition-delay: 0s; */
  }

  .card-effect:hover {
    box-shadow: none;
    transform: translateY(5px);
  }

  .cards-wrapper .service {
    position: relative;
    z-index: 2;
  }

  .service-img {
    height: 100px;
  }
</style>
