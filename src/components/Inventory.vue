<template>
  <div class="inventory">
    <v-row no-gutters justify="center" class="rowInventory" align="center">
      <v-col justify="center" align="center" cols="4">
        <v-progress-circular
          rotate="360"
          size="90"
          width="12"
          value="40"
          color="grey"
        >
        </v-progress-circular>
      </v-col>
      <v-col justify="center" align="center" cols="8">
        <div class="flexCol">
          <div class="subtitle">Current Inventory</div>
          <div class="flexRow">
            <div class="number">400</div>
            <v-btn class="text-capitalize" outlined small text tile
              >Manage Inventory</v-btn
            >
          </div>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "inventory",
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
  text-align: left;
}
.rowInventory {
  height: 100%;
  width: 100%;
}

.flexRow {
  justify-content: space-between;
  align-items: center;
  flex-direction: row;
  display: flex;
}

.flexCol {
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  height: 100% !important;
}
</style>