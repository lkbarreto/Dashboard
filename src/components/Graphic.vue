<script>
import { Bar, mixins } from "vue-chartjs";
Chart.defaults.global.legend.display = false;
Chart.defaults.scale.gridLines.display = false;
export default {
  extends: Bar,
  
  
  mounted() {
    this.renderChart(
      {
        
        labels: [
          "Jan",
          "Feb",
          "Mar",
          "Apr",
          "May",
          "Jun",
          "Jul",
          "Aug",
          "Sep",
          "Oct",
          "Nov",
          "Dec",
        ],
        datasets: [
          {
            barThickness: 15,
            backgroundColor: "#E3E4E5",
            data: [40, 20, 22, 39, 65, 40, 39, 75, 45, 25, 12, 35],
          },
        ],
      },
      { responsive: true, maintainAspectRatio: false }
    );
  },
};
</script>

<style>
</style>