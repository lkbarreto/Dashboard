<template>
  <div>
    <div class="flexRow">
      <div class="subtitle">Total gifts sent this year</div>
      <v-btn
        class="text-capitalize"
        outlined
        :small="size != 'sm' && size != 'xs'"
        :x-small="size == 'sm' || size == 'xs'"
        text
        tile
        >Download report</v-btn
      >
    </div>
    <div class="px-5">
      <Graphic />
    </div>
  </div>
</template>

<script>
import Graphic from "./Graphic";
export default {
  name: "Gifts",
  components: {
    Graphic,
  },
  computed: {
    size() {
      return this.$vuetify.breakpoint.name;
    },
  },
};
</script>

<style scoped>
.flexRow {
  justify-content: space-between;
  margin-bottom: 4vh;
  align-items: center;
  flex-direction: row;
  display: flex;
}
</style>