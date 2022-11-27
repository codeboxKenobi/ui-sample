<template>
    <span class="logo-ui-cmp">
        QX_Service
    </span>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
@import '~/src/assets/styles/custom.scss';

.logo-ui-cmp {
    @include flexRow( flex-start, center );
    @include font( 26px );
    height: 100%;
    margin: 0px 10px 0px 10px;
}
</style>