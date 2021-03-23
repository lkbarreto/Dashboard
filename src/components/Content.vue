<template>
  <div class="Content">
    <h1 class="title mb-10">Welcome to Gemnote, Ashley!</h1>
    <v-row class="mb-8" align="center" justify="center">
      <v-col align="center" justify="center" cols="12" sm="6">
        <v-card
          class="cardAverage pa-5"
          tile
          outlined
          width="100%"
          height="17vh"
        >
          <Averages />
        </v-card>
      </v-col>
      <v-col align="center" justify="center" cols="12" sm="6">
        <v-card
          class="cardAverage pa-3 flex"
          tile
          outlined
          width="100%"
          height="17vh"
        >
          <Inventory />
        </v-card>
      </v-col>
    </v-row>
    <v-row class="mb-10" align="center" justify="center">
      <v-card
        class="cardAverage pa-5"
        align="center"
        justify="center"
        tile
        outlined
        width="97%"
      >
        <Trending />
      </v-card>
    </v-row>
    <v-row align="center" justify="center">
      <v-card
        align="center"
        justify="center"
        tile
        outlined
        width="97%"
        height="100px"
      >
        4
      </v-card>
    </v-row>
  </div>
</template>

<script>
import Averages from "./AverageNumbers";
import Inventory from "./Inventory";
import Trending from "./Trending";
export default {
  name: "content",
  components: {
    Averages,
    Inventory,
    Trending,
  },
};
</script>

<style>
.v-application .title {
  font-size: 2rem !important;
  font-weight: 500;
  line-height: 2rem;
  letter-spacing: 0.0125em !important;
  font-family: "Roboto", sans-serif !important;
}

.cardAverage {
  justify-content: center;
  align-items: center;
}
</style>