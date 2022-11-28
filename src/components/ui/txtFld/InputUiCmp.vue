<template>
    <input class="input-ui-cmp" 
        type="text" 
        v-model="value"
        :placeholder="placeholder"
            @input="$emit( 'search-value', value )" >
</template>

<script>
    export default {
        props: {
            placeholder: { type: String, default: 'placeholder' }
        },

        data() {
            return {
                value: ''
            }
        }
    }
</script>

<style lang="scss" scoped>
@import '~/src/assets/styles/custom.scss';

.input-ui-cmp {
    height: 30px;
    width: 90%;
    padding: 0px 10px;
    border: $main-border1;
    outline: none;
}
</style>