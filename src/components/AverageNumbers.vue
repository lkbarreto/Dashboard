<template>
  <div class="averages pl-4">
    <v-row justify="center" class="rowAve pt-2" align="center">
      <v-col cols="6">
        <div class="subtitle">Total number of orders this month</div>
        <div class="number">2,366</div>
      </v-col>

      <v-col cols="6">
        <div class="subtitle">Average number of shipments/month</div>
        <div class="flexRow">
          <div class="number">364</div>
          <v-btn
            class="text-capitalize"
            outlined
            :small="size != 'sm' && size != 'xs'"
            :x-small="size == 'sm' || size == 'xs'"
            text
            tile
            >View orders</v-btn
          >
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "averages",
  computed: {
    size() {
      return this.$vuetify.breakpoint.name;
    },
  },
};
</script>

<style>
.averages {
  justify-content: space-between;
  align-items: center;
  display: flex;
  height: 100%;
}
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

@media only screen and (max-width: 768px) {
  .subtitle {
    font-size: 0.5em;
    font-weight: 400;
    margin-bottom: 1vh;
    text-align: justify;
  }
}

.rowAve {
  height: 100%;
}

.flexRow {
  justify-content: space-between;
  align-items: center;
  flex-direction: row;
  display: flex;
}
</style>