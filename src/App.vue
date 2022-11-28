<template>
  <header-cmp />
  <main-cmp />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HeaderCmp from './components/HeaderCmp.vue';
import MainCmp from './components/MainCmp.vue'

@Options({
  components: {
    HeaderCmp,
    MainCmp
  },
})

export default class App extends Vue {}
</script>

<style lang="scss">
@import '~/src/assets/styles/custom.scss';

#app {
  @include flexCol( flex-start, center );
  height: 100vh;
}

</style>
