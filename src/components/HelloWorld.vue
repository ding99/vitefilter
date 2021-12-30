
<template>
  <div>
    <h2>Filter learnVue Articles</h2>
    <input type='text' placeholder='Filter Search' v-model='query' />
    <br />
    <button @click='reset'> Reset </button>
    <br />
    <search-results :query='query' />
    <!-- {{ query }} -->
  </div>
</template>

<script>
import { ref } from 'vue'
import SearchResults from './SearchResults.vue'

export default {
  components: {
    SearchResults
  },

  setup () {
    const query = ref ('');

    const reset = (evt) => {
      query.value = ''  // clears the query
    }

    return {
      reset,
      query
    }
  }
}
</script>

<style>
    input[type='text'] {
      margin-bottom: 24px;
      padding: 12px;
    }
</style>