<template>
    <Transition name="slide">
        <div class="col-12" id="SideMenu"
            v-if="this.$store.state['CurrentWidth'] < 767 && this.$store.state['SideMenuIndex'] == 1">
            <div id="CloseMenuDiv" @click="this.$store.state['SideMenuIndex'] = 0">
                <font-awesome-icon id="CloseMenuIcon" icon="fa-solid fa-x" />
            </div>
            <ul id="TheMenuActions">
                <li>Hello</li>
                <li>Hello</li>
                <li>Hello</li>
                <li>Hello</li>
                <li>Hello</li>
            </ul>
        </div>
    </Transition>
</template>
  
<script>
// @ is an alias to /src

export default {
    name: 'SideMenu',
    components: {},
    data() {
        return {
            Api_Url: this.$store.state['Api_Url'],
        };
    },
    created() {

    },
    mounted() { },
    computed() { },
    watch: {}
}
</script>
  
<style lang="scss" scoped>
#SideMenu {
    height: 100vh;
    position: fixed;
    z-index: 2;
    top: 0;
    background-color: rgb(16, 16, 16);
    color: white;
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    justify-content: center;
    align-items: center;

    #CloseMenuDiv {
        padding: 0.5rem;
        border: 1px solid;
        border-radius: 50%;
        display: flex;
        cursor: pointer;
        transition: all ease 400ms;

        #CloseMenuIcon {
            width: 1.2rem;
            height: 1.2rem;
            font-size: 1.2rem;
            transition: all ease 400ms;
        }
    }

    #CloseMenuDiv:hover {
        background-color: rgb(241, 48, 80);
    }

    #CloseMenuDiv:hover>#CloseMenuIcon {
        color: black;
    }


    #TheMenuActions {
        padding: 0;
        margin: 0;
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;
        align-content: center;
        justify-content: center;
        align-items: flex-start;

        li {
            padding-top: 2rem;
            font-size: 1.5rem;
            list-style: none;
            transition: ease all 300ms;
            color: white;
            cursor: pointer;
        }

        li:hover {
            color: rgb(89, 89, 89);
        }
    }

}

.slide-enter-from {
    width: 0;
}

.slide-enter-to {
    width: 100%;
}

.slide-enter-active {
    transition: all 400ms ease;
}

.slide-leave-from {
    width: 100%;
}

.slide-leave-to {
    width: 0;
}

.slide-leave-active {
    transition: all 400ms ease;
}
</style>