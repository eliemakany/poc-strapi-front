<template>
  <div>
    <div v-for="(content, index) in contents" :key="index">
      <TwoCols v-if="content.__typename === 'ComponentTexte2Colonnes'" v-bind:content="content"></TwoCols>
      <ThreeCols v-if="content.__typename === 'ComponentTexte3Colonnes'" v-bind:content="content"></ThreeCols>
    </div>
  </div>
</template>

<script>

import TwoCols from '@/components/pagebuildercomponents/TwoCols.vue';
import ThreeCols from '@/components/pagebuildercomponents/ThreeCols.vue';

export default {
  props: {
    contents: Object
  },
  components : {
    TwoCols, ThreeCols
  },
  data () {
    return {
      pagesComponents: []
    }
  }
}

</script>

<style scoped>

</style>