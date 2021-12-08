<template>
  <div class="container">
    <h1 class="py-5 text-center"><b>Mental Health Statistics (2017)</b></h1>
    <div class="row">
      <div class="col-sm-6">
        <canvas id="myChart" ref="myChart"></canvas>
      </div>
      <div class="mt-3 col-sm-6">
        <canvas id="lineChart" ref="lineChart"></canvas>
      </div>
    </div>

    <div class="row mt-2">
      <div class="col-sm-6">
        <h4>Statistics for individual mental illness types</h4>
      </div>

      <div class="col-sm-6">
        <h4>Statistics for suicide rate (USA)</h4>
      </div>
    </div>

    <div class="row">
      <div class="col animation">
        <h1 class="mt-5">792 million</h1>

        <h4 class="my-5">
          There are about <b><u>792 million</u></b> people suffering from mental
          health diseases. Sucide rates are generally on the rise every year.
        </h4>

        <h4><b>Let us normalise this..</b></h4>

        <h4>Scroll down to find out how</h4>
      </div>
    </div>
  </div>
</template>

<script>
  import Chart from "chart.js/auto";

  export default {
    name: "Statistics",

    data() {
      return {};
    },
    //  Mounted function to display chart.js
    mounted() {
      // Graph 1
      let chart = this.$refs["myChart"].getContext("2d");
      let mentalHealthChart = new Chart(chart, {
        type: "bar",

        data: {
          labels: [
            "Depression",
            "Anxiety Disorders",
            "Alcohol use disorder",
            "Drug use disorder",
            "Bipolar disorder",
          ],
          datasets: [
            {
              label: "Numbers in millions",
              data: [264, 284, 107, 71, 46],
              backgroundColor: ["rgba(73,192,12,0.6)"],
            },
          ],
        },

        options: {},
      });

      console.log(mentalHealthChart);

      // Graph 2
      let chartTwo = this.$refs["lineChart"].getContext("2d");
      let mentalHealthChartTwo = new Chart(chartTwo, {
        type: "line",

        data: {
          labels: [
            "1999",
            "2000",
            "2001",
            "2002",
            "2003",
            "2004",
            "2005",
            "2006",
            "2007",
            "2008",
            "2009",
            "2010",
            "2011",
            "2012",
            "2013",
            "2014",
            "2015",
            "2016",
            "2017",
            "2018",
            "2019",
          ],
          datasets: [
            {
              label: "Sucide Rate Per 100,000",
              data: [
                10.5, 10.4, 10.7, 11.0, 10.8, 11.0, 11.3, 11.6, 11.8, 12.1,
                12.3, 12.5, 12.6, 13.0, 13.3, 13.4, 14.0, 14.2, 13.9,
              ],
              backgroundColor: ["rgba(223,12,12,0.6)"],
            },
          ],
        },
        options: {},
      });
      return mentalHealthChartTwo, mentalHealthChart;
    },
  };
</script>

<style scoped>
  * {
    /* color: white; */
    font-family: "Playfair Display", serif;
  }

  .animation h1 {
    background: orange;
    width: auto;
    display: inline-block;
    overflow: hidden;
    border-right: 0.15em solid white;
    white-space: nowrap;
    margin: 0 auto;
    letter-spacing: 0.15em;
    animation: typing 5s steps(100, end), blink-caret 1s step-end infinite;
    animation-iteration-count: infinite;
  }

  @keyframes typing {
    from {
      max-width: 0;
    }
    to {
      max-width: 100%;
    }
  }
  /* The typewriter cursor effect */

  @keyframes blink-caret {
    from,
    to {
      border-color: transparent;
    }
    50% {
      border-color: black;
    }
  }
</style>
