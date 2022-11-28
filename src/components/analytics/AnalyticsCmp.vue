<template>
    <div class="analytics-cmp">
        
    </div>
</template>

<script>
    export default {
        props: {
            // tableDadta: { type: Array, default: () => { return [] } }
        },

        data() {
            return {

            }
        },

        mounted() {
            console.log( this.tableDadta );
        },

        methods: {
            
        }
    }
</script>

<style lang="scss" scoped>
@import '~/src/assets/styles/custom.scss';

.analytics-cmp {
    @include flexRow( center, center );
    height: 98%;
    width: 99%;
    border: $main-border1;
}
</style>