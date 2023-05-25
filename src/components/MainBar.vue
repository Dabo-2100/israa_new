<template>
    <div class="col-12 animate__animated animate__fadeInUp animate__slow" id="MainBar">
        <div class="col-12 UpperSide">
        </div>
        <div class="col-12 DownSide">
            <div id="SideMenuDiv" @click="this.$store.state['SideMenuIndex'] = 1"
                v-if="this.$store.state['CurrentWidth'] < 767">
                <font-awesome-icon id="SideMenuIcon" icon="fa-solid fa-bars" />
            </div>
            <div id="ActionsDiv" v-if="this.$store.state['CurrentWidth'] > 767">
                <ul>
                    <li>تسجيل الدخول</li>
                    <li>عضوية جديدة</li>
                </ul>
            </div>
            <div id="LogoDiv">
                <p>استشاري علاقات زوجية</p>
            </div>
        </div>
    </div>
</template>
  
<script>
// @ is an alias to /src

export default {
    name: 'MainBar',
    components: {},
    data() {
        return {
            Api_Url: this.$store.state['Api_Url'],
        };
    },
    created() {

    },
    mounted() { this.$store.state['MainBarHeight'] = document.getElementById('MainBar').offsetHeight; },
    computed() { },
    watch: {}
}
</script>
  
<style lang="scss" scoped>
#MainBar {
    width: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    position: fixed;
    top: 0;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    align-content: flex-start;
    transition: ease all 300ms;

    .UpperSide {
        background-color: green;
        display: flex;
        height: 2rem;
    }

    .DownSide {
        padding: 1rem 5%;
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        justify-content: space-between;
        align-items: center;

        #SideMenuDiv {
            border: solid 1px;
            padding: 0.5rem;
            display: flex;
            flex-direction: row;
            flex-wrap: nowrap;
            align-content: center;
            justify-content: center;
            align-items: center;
            transition: ease all 300ms;
            cursor: pointer;

            #SideMenuIcon {
                color: white;
                height: 1.2rem;
                width: 1.2rem;
                font-size: 1.2rem;
                transition: ease all 300ms;
            }
        }

        #SideMenuDiv:hover {
            background-color: #fdfdfd;
        }

        #SideMenuDiv:hover>#SideMenuIcon {
            color: black;
        }
    }
}
</style>