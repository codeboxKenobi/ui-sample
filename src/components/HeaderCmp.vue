<template>
    <div class="header-cmp">
        
        <div class="header-cmp-logo-section">
            <logo-ui-cmp />
        </div>

        <div class="header-cmp-nav-section">
            <nav-ui-cmp />
        </div>

        <div class="header-cmp-search-section">

        </div>

        <div class="header-cmp-control-section">

        </div>

    </div>
</template>

<script>
import LogoUiCmp from './ui/LogoUiCmp.vue'
import NavUiCmp from './ui/NavUiCmp.vue'
    export default {
        components: {
            LogoUiCmp,
            NavUiCmp
        }
    }
</script>

<style lang="scss" scoped>
@import '~/src/assets/styles/custom.scss';

.header-cmp {
    @include flexRow( flex-start, center );
    height: 50px;
    width: 100%;
    // background-color: $main-color;

    &-logo-section {
        height: 80%;
        width: 320px;
        margin: 5px;
        // background-color: #fff;
    }

    &-nav-section {
        @include flexRow( center, center );
        height: 80%;
        width: 30%;
        margin: 5px;
        // background-color: #fff;
    }

    &-search-section {
        height: 80%;
        width: 26%;
        margin: 5px;
        background-color: rgb(233, 193, 193);
    }

    &-control-section {
        height: 80%;
        width: 20%;
        margin: 5px;
        background-color: rgb(158, 209, 162);
    }
}
</style>