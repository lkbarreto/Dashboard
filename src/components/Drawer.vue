<template>
  <div class="Drawer">
    <v-navigation-drawer
      class="drawerContent px-14"
      color="#242b2b"
      v-model="drawer"
      app
    >
      <v-img class="mb-15" contain src="../assets/logoTest.png"></v-img>
      <div class="mb-8">
        <span class="name">Asheley won</span>
      </div>

      <v-divider class="mb-4 white" />
      <v-list>
        <v-list-item v-for="item in list" :key="item.name" link dark>
          <v-list-item-content>
            <v-list-item-title>{{ item.name }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar v-if="size !== 'lg'" class="transparent" elevation="0" tile app>
      <v-app-bar-nav-icon
        color="black"
        @click="drawer = !drawer"
      ></v-app-bar-nav-icon>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "Drawer",
  data: () => ({
    drawer: null,
    list: [
      {
        name: "Dashboard",
        link: "",
      },
      {
        name: "Orders",
        link: "",
      },
      {
        name: "Send a gift",
        link: "",
      },
      {
        name: "Users",
        link: "",
      },
      {
        name: "Integrations",
        link: "",
      },
      {
        name: "Settings",
        link: "",
      },
      {
        name: "Logout",
        link: "",
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
.drawerContent {
  padding-top: 10vh;
}

.name {
  font-size: 1rem !important;
  letter-spacing: 0.0125em !important;
  font-family: "Roboto", sans-serif !important;
  color: white;
}
</style>