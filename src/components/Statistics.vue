<template>

<div class='container'>
      <canvas id="myChart" ref="myChart"></canvas>


</div>
    
</template>


<script>
import Chart from 'chart.js/auto';

export default{ 



    name: "Statistics",

    data(){
        return{

        }
    },
    //  Mounted function to display chart.js
    mounted() {

        let chart= this.$refs["myChart"].getContext("2d");
        let mentalHealthChart = new Chart(chart,{
            type:"bar",

            data:{
                labels: ["Depression",  "Anxiety Disorders", "Alcohol use disorder", "Drug use disorder","Bipolar disorder"],
                datasets:[{
                    label: "Numbers in millions",
                    data:[264, 284 , 107, 71, 46]



                }]

            },
            options:{}
        })

        console.log(mentalHealthChart)



    }
}


</script>



<style scoped>

</style>