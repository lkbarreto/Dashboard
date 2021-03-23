<template>
  <div class="Content">
    <h1 class="title mb-10">Welcome to Gemnote, Ashley!</h1>
    <v-row class="mb-8" align="center" justify="center">
      <v-col align="center" justify="center" cols="12" sm="6">
        <v-card tile outlined width="95%" height="100px">1</v-card>
      </v-col>
      <v-col align="center" justify="center" cols="12" sm="6">
        <v-card tile outlined width="95%" height="100px"> 2 </v-card>
      </v-col>
    </v-row>
    <v-row class="mb-10" align="center" justify="center">
      <v-card
        align="center"
        justify="center"
        tile
        outlined
        width="95%"
        height="100px"
      >
        3
      </v-card>
    </v-row>
    <v-row align="center" justify="center">
      <v-card
        align="center"
        justify="center"
        tile
        outlined
        width="95%"
        height="100px"
      >
        4
      </v-card>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "content",
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
</style>