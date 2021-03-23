<template>
  <div class="averages">
    <v-row  justify="center" class="rowAve" align="center">
      <v-col cols="5">
        <div class="subtitle">Total number of orders this month</div>
        <div class="number">2,366</div>
      </v-col>
      <v-col cols="7">
        <div class="subtitle">Average number of shipments/month</div>
        <div class="flexRow">
          <div class="number">364</div>
          <v-btn class="text-capitalize" outlined  small text tile>View orders</v-btn>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "averages",
};
</script>

<style>
.number {
  font-size: 1.5em;
  font-weight: 500;
  text-align: left;
}
.subtitle {
  font-size: 0.8em;
  font-weight: 500;
  margin-bottom: 1.2vh;
  text-align: left;
}
.rowAve {
  height: 60%;
  width: 100%;
}

.flexRow {
  justify-content: space-between;
  align-items: center;
  flex-direction: row;
  display: flex;
}
</style>