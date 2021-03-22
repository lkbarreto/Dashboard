<template>
  <div class="Drawer">
    <v-navigation-drawer color="#242b2b" v-model="drawer" app>
      <!--  -->
    </v-navigation-drawer>
    <v-app-bar v-if="size !== 'lg'" class="transparent" elevation="0" tile app>
      <v-app-bar-nav-icon
        color="black"
        @click="drawer = !drawer"
      ></v-app-bar-nav-icon>

      <v-toolbar-title>{{ size }}</v-toolbar-title>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "Drawer",
  data: () => ({ drawer: null }),
  computed: {
    size() {
      return this.$vuetify.breakpoint.name;
    },
  },
};
</script>

<style>
</style>