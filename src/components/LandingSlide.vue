<template>
    <div class="col-12" id="LandingSlide">
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
    methods: {},
    computed() { },
    watch: {},
}
</script>
  
<style lang="scss" scoped>
#LandingSlide {
    height: 100vh;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-content: flex-start;
    background-color: azure;
}
</style>