<template>
  <li v-for="record in weightRecords" :key="record.id">
    <div>
      <base-card>
        <span><strong>Weight</strong></span>
        <span> {{ record.weight }}</span>
        <span><strong>Date</strong></span>
        <span> {{ record.date }}</span>
      </base-card>
    </div>
  </li>
</template>
<script>
export default {
  props: ["weightRecords"],
  data() {
    return {
      editable: false,
    };
  },
};
</script>
<style scoped>
div {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  text-align: center;
}
span {
  display: inline-block;
  margin: 0.3rem;
}
</style>
