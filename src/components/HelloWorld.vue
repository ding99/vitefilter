
<template>
  <div>
    <h2>Filter learnVue Articles</h2>
    <input type="text" placeholder="Filter Search" v-model="query" />
    <button @click="reset">Reset</button>
    <br/>
    {{ query }}
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const query = ref("");

    const reset = (evt) => {
      query.value = "";  // clears the query
    }

    return {
      reset,
      query,
    };
  },
};
</script>
