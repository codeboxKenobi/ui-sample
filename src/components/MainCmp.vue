<template>
    <div class="main-cmp">
        <table-ui-cmp v-if="tableCmp" :tableData="tableData" />
        <analytics-cmp v-if="analyticsCmp" />
    </div>
</template>

<script>
import TableUiCmp from './ui/tbl/TableUiCmp.vue'
import AnalyticsCmp from'./analytics/AnalyticsCmp.vue'

    export default {
        data() {
            return {
                tableCmp: true,
                analyticsCmp: false,

                tableData: [
                    { 
                        number: '1' ,
                        status: 'Новый заказ',
                        name: 'Писарев Михаил',
                        telNumber: '+7 978 654 32 55',
                        reason: 'Замена аккумулятора',
                        deviceType: 'Смартфон',
                        deviceManufacturer: 'Xiaomi',
                        deviceModel: 'Redmi Note 7',
                        serviceCost: 2400,
                    },
                    { 
                        number: '2' ,
                        status: 'Новый заказ',
                        name: 'Писарева Мария',
                        telNumber: '+7 978 576 33 75',
                        reason: 'Замена аккумулятора',
                        deviceType: 'Смартфон',
                        deviceManufacturer: 'Xiaomi',
                        deviceModel: 'Redmi Note 7',
                        serviceCost: 2400,
                    },
                    { 
                        number: '3' ,
                        status: 'Новый заказ',
                        name: 'Писарев Михаил',
                        telNumber: '+7 978 654 32 55',
                        reason: 'Замена аккумулятора',
                        deviceType: 'Смартфон',
                        deviceManufacturer: 'Xiaomi',
                        deviceModel: 'Redmi Note 7',
                        serviceCost: 2400,
                    },
                    { 
                        number: '4' ,
                        status: 'Новый заказ',
                        name: 'Писарев Михаил',
                        telNumber: '+7 978 654 32 55',
                        reason: 'Замена аккумулятора',
                        deviceType: 'Смартфон',
                        deviceManufacturer: 'Xiaomi',
                        deviceModel: 'Redmi Note 7',
                        serviceCost: 2400,
                    }
                ]
            }
        },

        components: {
            TableUiCmp,
            AnalyticsCmp
        },
    }
</script>

<style lang="scss" scoped>
@import '~/src/assets/styles/custom.scss';

.main-cmp {
    @include flexRow( center, center );
    height: calc( 100vh - 50px );
    width: 100%;
}
</style>