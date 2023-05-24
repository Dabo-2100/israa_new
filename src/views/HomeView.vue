<template>
  <div class="col-12" id="HomeView">
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
  created() { },
  mounted() { },
  computed() { },
  watch: {}
}
</script>

<style lang="scss" scoped>
#HomeView {
  display: flex;
  width: 100%;
}
</style>