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

@media only screen and (max-width: 768px) {
  .content {
  padding-top: 2vh;
  padding-left: 7vw;
  padding-right: 7vw;
}
}

</style>
