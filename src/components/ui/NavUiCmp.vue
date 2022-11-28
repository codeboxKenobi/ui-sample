<template>
    <div class="nav-ui-cmp">
        <tab-ui-cmp :amount="navTabs.length"  
            v-for="( navTab, navTabIndex ) in navTabs" 
                :class="active === navTabIndex 
                    ? 'active-tab' 
                    : '' "
                :key="navTabIndex"
                :btnName="Object.values( navTab )[ 0 ]"
                :id="Object.keys( navTab )"
                    @click="active = navTabIndex"
                    @click-handler="clickHandler( navTab )" />
    </div>
</template>

<script>

import TabUiCmp from './btn/TabUiCmp.vue'
import { navTabs } from '/src/assets/data/ui-nav-data.js'

    export default {
        data() {
            return {
                navTabs,
                active: false
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
}
</style>