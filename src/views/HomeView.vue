<template>
  <div class="col-12" id="HomeView" :style="'padding-top : ' + this.$store.state['MainBarHeight'] + 'px;'">
    <h1 class="col-12">This is Home View</h1>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'HomeView',
  components: {},
  data() {
    return {
      Api_Url: this.$store.state['Api_Url'],
    };
  },
  created() {
    this.$store.state['LoaderIndex'] = 1;
    setTimeout(() => {
      this.$store.state['LoaderIndex'] = 0;
    }, 1500);
  },
  mounted() { },
  computed() { },
  watch: {}
}
</script>

<style lang="scss" scoped>
#HomeView {
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-content: flex-start;
}
</style>