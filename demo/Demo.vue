<template>
  <div class="container">
    <h2>Demo</h2>
    <TwentyTwenty
      v-model="offset"
      keyboardStep="0.1"
      before="//placehold.it/600x200/E8117F/FFFFFF"
      beforeLabel="before"
      after="//placehold.it/600x200/CCCCCC/FFFFFF"
      afterLabel="after" />
  </div>
</template>

<script>
  import TwentyTwenty from '../src/TwentyTwenty.vue';

  export default {
    components: {
      TwentyTwenty
    },
    data() {
      return {
        offset: 0.7
      }
    }
  }
</script>

<style>
  .container {
    margin: 0 auto;
    width: 80%;
    font-family: sans-serif;
  }
  .container img {
    max-width: 100%;
  }
</style>
