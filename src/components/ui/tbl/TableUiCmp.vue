<template>
    <div class="table-ui-cmp">
        <table-group :serviceTablesCol="serviceTablesCol" 
            :tableData="tableData" />
    </div>
</template>

<script>
import { serviceTablesCol } from '/src/assets/data/ui-table-data.js'
import TableGroup from './TableGroup.vue'

    export default {
        props: {
            tableData: { type: Array, default: () => { return [] } }
        },

        data() {
            return {
                serviceTablesCol
            }
        },

        components: {
            TableGroup
        },

        mounted() {
            console.log( this.tableData );
        }
    }
</script>

<style lang="scss" scoped>
@import '~/src/assets/styles/custom.scss';

.table-ui-cmp {
    @include flexRow( center, center );
    height: 98%;
    width: 99%;
    border: $main-border1;
}
</style>