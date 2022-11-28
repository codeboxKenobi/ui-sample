<template>
  <header-cmp />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HeaderCmp from './components/HeaderCmp.vue';

@Options({
  components: {
    HeaderCmp
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
