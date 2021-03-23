<script>
import { Bar, mixins } from "vue-chartjs";
Chart.defaults.global.legend.display = false;
export default {
  extends: Bar,
  mixins: [mixins.reactiveProp],
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
            barThickness: 16,
            backgroundColor: "grey",
            data: [40, 20, 12, 39, 10, 40, 39, 80, 40, 20, 12, 11],
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