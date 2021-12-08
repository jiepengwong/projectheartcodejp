<template>
  <h1 class="py-5"><b>Ask for assistance</b></h1>
  <h5>
    <i>If you need to talk to someone about what you are experiencing, do not
    hesitate to reach out. With helplines available for you to call, you can
    speak about the issues affecting you and get help that you may need.</i>
  </h5>
  <div class="container">
    <div class="row">
      <div v-for="card in cards" :key="card" class="col-md-4 my-4">
        <div class="card mx-auto">
          <img
            style="height: 200px"
            :src="require(`../assets/${card.imgName}.png`)"
            class="card-img-top"
            alt="..."
          />
          <div class="card-body">
            <h5 class="card-title">{{card.title}}</h5>

              <a class="details"
                data-bs-toggle="collapse"
                :href="`#${card.imgName}`"
                role="button"
                aria-expanded="false"
                :aria-controls="card.imgName"
              >
                More details
              </a>

              <div class="bottom">
                <p :id="card.imgName" class="card-text text-start collapse">
                  {{ card.description }}
                  
                  <br>
                  <a :href="card.url" class="btn btn-primary mt-3">Find out more</a>
                </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "HelpLine",

    data() {
      return {
        cards: [
          {
            title: "Silver Ribbon",
            imgName: "silverribbon",
            description:
              "Silver Ribbon (Singapore) tries to combat the stigma with counselling services and mental wellness workshops – these are customised according to the audience, which ranges from students to working adults and senior citizens.",
            url: "https://www.silverribbonsingapore.com/",
          },
          {
            title: "Samaritans of Singapore",
            imgName: "sos",
            description:
              "Samaritans of Singapore (SOS) is dedicated to providing confidential emotional support to individuals facing a crisis, thinking about or affected by suicide. Non-religious and not for profit, their work focuses on crisis intervention and suicide prevention.",
            url: "https://www.sos.org.sg/",
          },
          {
            title: "Over The Rainbow",
            imgName: "rainbow",
            description:
              "Over The Rainbow is a Singapore non-profit offering free mental health resources for youth with a focus on developing self-care. The volunteer-driven effort has shared numerous resources online and organised workshops to teach alternative and creative therapies to improve mental wellness and resilience",

            url: "http://overtherainbow.sg/?fbclid=IwAR275R-WXU414nLV3l5K0ptYsZUGMWezM3JNaLBPmzIZpskdy1e9X9UJYOs",
          },

          {
            title: "Annabelle Psychology",
            imgName: "annabelle",
            description:
              "Annabelle Psychology is a mental health group practice located in Singapore providing therapy to adults, children, couples and families. Our psychologists work closely with psychiatrists, paediatricians and other professionals to provide holistic care to complex presentations.",

            url: "http://overtherainbow.sg/?fbclid=IwAR275R-WXU414nLV3l5K0ptYsZUGMWezM3JNaLBPmzIZpskdy1e9X9UJYOs",
          },

          {
            title: "Club HEAL",
            imgName: "clubheal",
            description:
              "Club HEAL (Hope, Empowerment, Acceptance & Love) aims to assist and empower persons with mental health issues to regain confidence in themselves and others in their journey towards community reintegration.",

            url: "http://overtherainbow.sg/?fbclid=IwAR275R-WXU414nLV3l5K0ptYsZUGMWezM3JNaLBPmzIZpskdy1e9X9UJYOs"
          },

          {
            title: "Campus PSY",
            imgName: "campuspsy",
            description:
              "Campus PSY (Peer Support for Youths) provides a support group for those passionate in starting change in the Youth Mental Health space in Singapore. Youth volunteers are trained in advocacy and equipped with basic mental health literacy and peer helping skills to better support fellow peers who might be in distress or suffering from mental health issues in school or at the workplace.",

            url: "https://www.facebook.com/campuspsy"
          },


        //   {
        //     title: "Campus PSY",
        //     imgName: "campuspsy",
        //     description:
        //       "Campus PSY (Peer Support for Youths) provides a support group for those passionate in starting change in the Youth Mental Health space in Singapore. Youth volunteers are trained in advocacy and equipped with basic mental health literacy and peer helping skills to better support fellow peers who might be in distress or suffering from mental health issues in school or at the workplace.",

        //     url: "https://www.facebook.com/campuspsy",
        //   }
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
  .card:hover {
    transform: scale(1.05);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12), 0 4px 8px rgba(0, 0, 0, 0.06);
  }

  .details{
      text-decoration: none;
      background-color: #ddd;
  border: none;
  color: black;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 16px;
  }

  .details:hover{
    background: #00c2cb;
    color: white;

  }

  .btn-primary{
       background: #00c2cb;
        color: white;

  }
</style>
