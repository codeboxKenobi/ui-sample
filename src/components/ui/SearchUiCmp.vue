<template>
    <div class="search-ui-cmp">
        <input-ui-cmp placeholder="Найти"
            @search-value="searchValue" />
    </div>
</template>

<script>
import InputUiCmp from '../ui/txtFld/InputUiCmp.vue'

    export default {
        components: { 
            InputUiCmp 
        },

        methods: {
            searchValue( data ) {
                console.log( data );
            }
        }
    }
</script>

<style lang="scss" scoped>
@import '~/src/assets/styles/custom.scss';

.search-ui-cmp {
    @include flexRow( center, center );
    height: 100%;
    width: 100%;
}
</style>