<template>
    <button type="button" 
        class="tab-ui-cmp"
            @click="$emit( 'click-handler' )">
        {{ btnName }}
    </button>
</template>

<script>
    export default {
        props: {
            btnName: { type: String, default: 'btn' },
            amount: { type: Number, default: 0 }
        },
    }
</script>

<style lang="scss" scoped>
@import '~/src/assets/styles/custom.scss';

.tab-ui-cmp {
    @include font( 14px );
    height: 90%;
    width: 24%;
    border: none;
    outline: none;

    &:hover {
        background-color: $main-color;
        color: $main-white;
    }
}
</style>