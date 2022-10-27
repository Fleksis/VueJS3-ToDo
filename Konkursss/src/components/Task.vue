<template>
  <div ref="task" id="task">
    <h5>{{ title }}</h5>
    <p v-show="description">{{ description }}</p>
    <LabelsComponent :title="label" />
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

#task > p,
#task > h5 {
  margin: 0;
}

#task > h5:first-child {
  color: white;
  font-family: SF-Pro-Display-Bold;
  font-weight: lighter;
  font-size: 16px;
}

#task > p:nth-child(2) {
  font-family: SF-Pro-Display-Regular;
  line-height: 140%;
  font-size: 14px;
  color: rgba(255, 255, 255, 0.75);
}
</style>
