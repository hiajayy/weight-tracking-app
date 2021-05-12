<template>
  <button :class="mode">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: ["mode"],
};
</script>
<style scoped>
button {
  font-size: 18px;
  padding: 0.6rem 0.8rem;
  border: none;
  background-color: var(--pink-color);
  color: #fff;
  cursor: pointer;
  transition: all 300ms ease-in-out;
}
button:hover {
  background-color: var(--orange-color);
}
.nav {
  background-color: var(--primary-color);
}
</style>
