<template>
    <div class="header-cmp">
        
        <div class="header-cmp-logo-section">
            <logo-ui-cmp />
        </div>

        <div class="header-cmp-nav-section">
            <nav-ui-cmp />
        </div>

        <div class="header-cmp-search-section">
            <search-ui-cmp />
        </div>

        <div class="header-cmp-control-section">
            <div class="header-cmp-control-section-account">
                Пользователь: kenobi@gmail.com
            </div>

            <div class="header-cmp-control-section-logout">
                <tab-ui-cmp btnName="Выйти"
                    @click-handler="clickHandler" />
            </div>
        </div>

    </div>
</template>

<script>
import LogoUiCmp from './ui/LogoUiCmp.vue'
import NavUiCmp from './ui/NavUiCmp.vue'
import SearchUiCmp from './ui/SearchUiCmp.vue'
import TabUiCmp from './ui/btn/TabUiCmp.vue'

    export default {
        components: {
            LogoUiCmp,
            NavUiCmp,
            SearchUiCmp,
            TabUiCmp
        },

        methods: {
            clickHandler() {
                console.log( 'Logout' );
            }
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
        @include flexRow( center, center );
        height: 80%;
        width: 26%;
        margin: 5px;
        // background-color: rgb(214, 123, 123);
    }

    &-control-section {
        @include flexRow( space-between, center );
        height: 80%;
        width: 25%;
        margin: 5px;
        // background-color: rgb(158, 209, 162);

        &-account {
            @include flexRow( flex-start, center );
            @include font( 10px );
            height: 30px;
            width: 60%;
            padding: 0px 10px;
            border: $main-border1;
            // background-color: rgb(207, 110, 110);
        }

        &-logout {
            @include flexRow( center, center );
            height: 80%;
            width: 30%;
            // background-color: rgb(181, 189, 70);
        }
    }
}
</style>