<template>
  <div class="home">
    <Drawer />
    <div class="content">
      <Content />
    </div>
  </div>
</template>

<script>
import Drawer from "../components/Drawer";
import Content from "../components/Content";
export default {
  name: "Home",
  components: {
    Drawer,
    Content,
  },
};
</script>


<style scoped>
.content {
  padding-top: 10vh;
  padding-left: 8vw;
  padding-right: 8vw;
}
</style>
