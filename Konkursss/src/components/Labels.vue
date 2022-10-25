<template>
  <div ref="label" id="label-container">
    <p>{{ title }}</p>
  </div>
</template>

<script>
export default {
  name: "LabelsComponent",
  props: ["title"],
  mounted() {
    if (!this.title) {
      this.$refs.label.style.display = "none";
    }
  },
};
</script>

<style scoped>
#label-container {
  width: fit-content;
  display: flex;
  align-items: center;
  padding: 2px 8px;
  border: solid 1px rgba(255, 255, 255, 0.75);
  border-radius: 2px;
  user-select: none;
}

#label-container > p {
  font-family: SF-Pro-Display-Regular;
  font-size: 14px;
  line-height: 140%;
  color: rgba(255, 255, 255, 0.75);
  margin: 0;
}
</style>
