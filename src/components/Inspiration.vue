<template>
  <h1 class="py-5"><b>Inspiration success stories</b></h1>
  <h4>
    Having a mental illness is tough, but with much resilience and dedication,
    it could be easily overcomed. These are some of the few success cases.
  </h4>
  <h4>
    The power to change lies within <span class="highlight"><b>YOU</b></span>. Do not
    give up.
  </h4>
  <div class="offerings">
    <div v-for="people in peoples" :key="people" class="offeringsItem">
      <div class="offeringsImg">
        <img :src="require(`../assets/${people.imageName}.png`)" />
        <h3>{{ people.person }}</h3>
        <h6><a class="details" :href="people.url" target="_blank">Read more</a></h6>
      </div>
      <div class="offeringsContent">
        <h5>{{ people.story }}</h5>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Inspiration",

    data() {
      return {
        peoples: [
          {
            person: "Will Wheaton",
            imageName: "willwheaton",
            story:
              "Wil Wheaton, New York Times Number One Bestselling Audiobook narrator and former Star Trek actor, tells his story of living with depression and anxiety, “the tag team champions of the World Wrestling With Mental Illness Federation”. The story shows that success and mental illness aren’t mutually exclusive.",
            url: "https://medium.com/@wilw/my-name-is-wil-wheaton-i-live-with-chronic-depression-and-generalized-anxiety-i-am-not-ashamed-8f693f9c0af1",
          },

          {
            person: "Damien Coates",
            imageName: "damiencoates",
            story:
              "Damien Coates is the CEO of DUAL Asia Pacific, and a proud supporter of Black Dog Institute. The entrepreneur here shares his experience on how he first encountered his panic attacks, what were his triggers and ultimately how he overcame it together with his friends and families.",
            url: "https://www.blackdoginstitute.org.au/resources-support/personal-stories/damien/",
          },

          {
            person: "David Ly Khim",
            imageName: "davidkhim",
            story:
              "David Ly Khim, a front end engineer, talks about his journey of relocation and how it lead to social isolation which was the root cause of his mental illness. In his story, David shares essential tips and tricks for people suffering from mental illnesses on how to live their best life.",
            url: "https://medium.com/@davidlykhim/a-reflection-on-how-i-dug-myself-out-of-the-millennial-mental-health-decline-831ae56e721c",
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
  .offeringsItem {
    display: flex;
    flex-wrap: wrap;
    /* margin: 10px; */
    padding: 15px;
    border-bottom: 2px solid black;
  }

  .offeringsItem:nth-of-type(even) {
    flex-flow: row-reverse;
  }

  .offeringsContent,
  .offeringsImg {
    /* margin: 10px; */
    padding: 20px;
  }

  .offeringsContent {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .offeringsImg h3 {
    margin-top: 10px;
  }

  .offeringsContent {
    flex: 1;
  }

  .offeringsImg img {
    max-width: 100%;
    border-radius: 100%;
    width: 300px;
    height: 300px;
  }

  .details {
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

  .details:hover {
    background: #00c2cb;
    color: white;
  }

  @media (max-width: 700px) {
    .offeringsItem {
      display: block;
    }
  }
</style>
