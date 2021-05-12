<template>
  <div>
    <ul>
      <single-weight :weightRecords="weightData"></single-weight>
    </ul>
  </div>
</template>
<script>
import SingleWeight from "./SingleWeight";
export default {
  components: {
    SingleWeight,
  },
  inject: ["weightData"],
  provide() {
    return {};
  },
};
</script>
<style scoped>
ul {
  display: flex;
  justify-content: space-evenly;
  list-style: none;
  padding: 1rem;
  flex-wrap: wrap;
}
</style>
