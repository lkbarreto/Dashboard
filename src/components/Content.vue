<template>
  <div class="Content mb-10">
    <h1 class="title">Welcome to Gemnote, Lourdes!</h1>
    <v-row class="mb-8" align="center" justify="center">
      <v-col align="center" justify="center" cols="12" sm="6">
        <v-card class="cardAverage" tile outlined width="100%" height="20vh">
          <Averages />
        </v-card>
      </v-col>
      <v-col align="center" justify="center" cols="12" sm="6">
        <v-card
          class="cardAverage flex"
          tile
          outlined
          width="100%"
          height="20vh"
        >
          <Inventory />
        </v-card>
      </v-col>
    </v-row>
    <v-row class="mb-10" align="center" justify="center">
      <v-card
        class="cardAverage"
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
        class="cardAverage"
        align="center"
        justify="center"
        tile
        outlined
        width="97%"
      >
        <Gifts />
      </v-card>
    </v-row>
  </div>
</template>

<script>
import Averages from "./AverageNumbers";
import Inventory from "./Inventory";
import Trending from "./Trending";
import Gifts from ".//Gifts";
export default {
  name: "contentComponent",
  components: {
    Averages,
    Inventory,
    Trending,
    Gifts,
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
  margin-bottom: 5vh;
}

.cardAverage {
  justify-content: center;
  align-items: center;
  padding: 2%;
  padding-left: 4%;
  padding-right: 4%;
}

@media only screen and (max-width: 768px) {
  .cardAverage {
    justify-content: center;
    align-items: center;
    padding: 3%;
  }
  .v-application .title {
  font-size: 1.6rem !important;
  font-weight: 500;
  line-height: 2rem;
  letter-spacing: 0.0125em !important;
  font-family: "Roboto", sans-serif !important;
  margin-bottom: 3vh;
}
}
</style>