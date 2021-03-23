<template>
  <div class="Trending">
    <div class="subtitle">Trending gifts in your store</div>
    <v-row no-gutters class="rowTrending" align="center">
      <v-col justify="center" align="center" cols="8">
        <v-row v-if="!size == 'sm' || !size == 'xs'">
          <v-col v-for="item in data" :key="item.id" cols="3">
            <v-item v-slot="{ toggle }">
              <v-img contain height="200px" :src="item.source" @click="toggle">
              </v-img>
            </v-item>
          </v-col>
        </v-row>

        <v-slide-group
          v-else
          v-model="model"
          class="pa-0"
          center-active
          show-arrows
          mandatory
        >
          <v-slide-item
            class="mx-0"
            v-for="item in data"
            :key="item.id"
            v-slot="{ toggle }"
          >
            <v-img
              contain
              width="100px"
              height="100px"
              :src="item.source"
              @click="toggle"
            >
            </v-img>
          </v-slide-item>
        </v-slide-group>
      </v-col>
      <v-col justify="center" align="center" cols="4">
        <v-btn
          class="text-capitalize float-right"
          outlined
          :x-small="size == 'sm' || size == 'xs'"
          text
          tile
          >Send a gift</v-btn
        >
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Trending",
  data: () => ({
    model: null,

    data: [
      {
        id: 1,
        source:
          "https://res.cloudinary.com/lou/image/upload/v1616470794/Tests/imagen1_nvm82m.png",
      },
      {
        id: 2,
        source:
          "https://res.cloudinary.com/lou/image/upload/v1616470793/Tests/imagen2_xoniqp.png",
      },
      {
        id: 3,
        source:
          "https://res.cloudinary.com/lou/image/upload/v1616470793/Tests/imagen3_v2dp55.png",
      },
      {
        id: 4,
        source:
          "https://res.cloudinary.com/lou/image/upload/v1616470792/Tests/imagen4_qpef49.png",
      },
    ],
  }),
  computed: {
    size() {
      return this.$vuetify.breakpoint.name;
    },
  },
};
</script>

<style>
.subtitle {
  font-size: 0.8em;
  font-weight: 500;
  text-align: left;
  margin-bottom: 2%;
}
</style>