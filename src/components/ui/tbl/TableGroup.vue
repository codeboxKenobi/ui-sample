<template>
    <div class="table-group">
        <div class="table-group-header">
            <div class="table-group-header-controls">
                <div class="table-group-header-controls-btn">
                    <tab-ui-cmp btnName="Новый заказ" />
                </div>
            </div>
        </div>

        <div class="table-group-table-section">

            <div class="table-group-table-section-item"
                v-for="( item, itemIndex) in tableData" :key="itemIndex"
                    @click="getOrderData( item )">

                <div class="table-group-table-section-item-description">
                    <div class="table-group-table-section-item-description-el" 
                        v-for="( descriptField, descriptFieldIdx ) in serviceTablesCol" 
                        :key="descriptFieldIdx" >
                        <span>
                            {{ Object.values( descriptField )[ 0 ] }}
                        </span>
                    </div>
                </div>
                
                <div class="table-group-table-section-item-value">
                    <div class="table-group-table-section-item-value-el" >
                        
                        <span class="table-group-table-section-item-value-el-val" 
                            v-for="( textItem, textIndex ) in item " 
                            :key="textIndex">
                            {{ textItem }}
                        </span>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>

<script>

import TabUiCmp from '../btn/TabUiCmp.vue'

    export default {
        props: {
            tableData: { type: Array, default: () => { return [] } },
            serviceTablesCol: { type: Array, default: () => { return [] } },
        },

        data() {
            return {

            }
        },

        components: {
            TabUiCmp
        },

        methods: {
            getOrderData( data ) {
                console.log( data );
            }
        }
    }
</script>

<style lang="scss" scoped>
@import '~/src/assets/styles/custom.scss';

.table-group {
    @include flexCol( flex-start, center );
    height: 100%;
    width: 100%;

    &-header {
        @include flexRow( flex-start, center );
        height: 40px;
        width: 100%;
        border-bottom: $main-border1;

        &-controls {
            @include flexRow( center, center );
            height: 90%;
            width: auto;

            &-btn {
                @include flexRow( center, center );
                width: 120px;
                margin: 0px 5px;
            }
        }
    }

    &-table-section {
        @include flexCol( flex-start, center );
        height: calc( 100% - 40px );
        width: 100%;

        &-item {
            @include flexCol( flex-start, center );
            height: 50px;
            width: calc( 100% - 10px );
            margin: 5px 0px 0px 0px;
            border: $main-border1;

            &:hover {
                background-color: $main-color-hover;
            }

            &-description {
                @include flexRow( space-between, center );
                margin-top: 5px;
                height: 30%;
                width: 100%;

                &-el:first-child {
                    @include flexRow( flex-start, center );
                    margin-left: 10px;
                }

                &-el {
                    @include flexRow( center, center );
                    @include font( 10px );
                    height: 90%;
                    width: 100%;
                }

                &-el:last-child {
                    margin-right: 10px;
                    @include flexRow( flex-end, center );
                }
            }

            &-value {
                @include flexRow( space-between, center );
                height: 70%;
                width: 100%;

                &-el:first-child {
                    @include flexRow( flex-start, center );
                    margin-left: 10px;
                }

                &-el {
                    @include flexRow( space-between, center );
                    @include font( 12px );
                    height: 90%;
                    width: 100%;

                    &-val:first-child {
                        @include flexRow( flex-start, center );
                        height: 100%;
                        width: 100%;
                    }

                    &-val {
                        @include flexRow( center, center );
                        height: 100%;
                        width: 100%;
                    }

                    &-val:last-child {
                        @include flexRow( flex-end, center );
                        height: 100%;
                        width: 100%;
                    }
                }

                &-el:last-child {
                    margin-right: 10px;
                    @include flexRow( flex-end, center );
                }
            }
        }
    }
}
</style>