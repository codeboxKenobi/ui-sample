<template>
    <div class="nav-ui-cmp">
        <tab-ui-cmp :amount="navTabs.length" :btnName="Object.values( navTab )[ 0 ]" 
            v-for="( navTab, navTabIndex ) in navTabs" 
                :key="navTabIndex"
                @click-handler="clickHandler( navTab )" />
    </div>
</template>

<script>
import TabUiCmp from './btn/TabUiCmp.vue'
import { navTabs } from '/src/assets/data/ui-data.js'

    export default {
        data() {
            return {
                navTabs
            }
        },

        components: { 
            TabUiCmp 
        },

        methods: {
            clickHandler( data ) {
                console.log( data );
            }
        }
    }
</script>

<style lang="scss" scoped>
@import '~/src/assets/styles/custom.scss';

.nav-ui-cmp {
    @include flexRow( space-between, center );
    height: 90%;
    width: 98%;
    // background-color: rgb(150, 94, 94);
}
</style>