<template>
  <div ref="task" id="task">
    <p>{{ title }}</p>
    <p>{{ description }}</p>
    <LabelsComponent  :title="label" />
  </div>
</template>

<script>
import LabelsComponent from "@/components/Labels.vue";
export default {
  name: "TaskComponent",
  components: { LabelsComponent },
  props: ["title", "description", "color", "label"],
  mounted() {
    this.$refs.task.style.backgroundColor = this.color;
  },
};
</script>

<style scoped>
#task {
  display: flex;
  flex-direction: column;
  gap: 8px;
  padding: 24px;
  border-radius: 8px;
}

#task > p {
  margin: 0;
}

#task > p:first-child {
  color: white;
  font-family: SF-Pro-Display-Bold;
  line-height: 150%;
}

#task > p:nth-child(2) {
  font-family: SF-Pro-Display-Regular;
  line-height: 140%;
  font-size: 14px;
  color: rgba(255, 255, 255, 0.75);
}
</style>
