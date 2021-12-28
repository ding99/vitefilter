
<template>
  <div>
    <h2>Filter learnVue Articles</h2>
    <input type="text" placeholder="Filter Search" v-model="query" />
    <br/>
    {{ query }}
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const query = ref("");

    return {
      query,
    };
  },
};
</script>
