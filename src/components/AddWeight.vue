<template>
  <div>
    <form @submit.prevent="submitData">
      <div class="form-group">
        <label for="weight">Enter your weight(kg)</label>
        <input
          type="text"
          id="weight"
          name="weight"
          class="form-control"
          ref="weight"
        />
      </div>
      <div>
        <base-button>Add Weight</base-button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  inject: ["addWeight"],
  methods: {
    submitData() {
      const weight = this.$refs.weight.value;
      const newRecord = {
        id: new Date().toISOString(),
        date: new Date().toDateString(),
        weight: weight,
      };
      this.addWeight(newRecord);
    },
  },
};
</script>

<style scoped>
div {
  padding: 1rem;
}
.form-group {
  display: flex;
  flex-direction: column;
}
label {
  margin-bottom: 0.5rem;
}
.form-control {
  font-size: 18px;
  padding: 0.3rem 0.5rem;
  border: 1px solid var(--secondary-color);
  line-height: 1.5;
}
.form-control:focus-visible {
  outline: 2px solid var(--secondary-color);
}
</style>
