<template>
  <div v-on="$listeners" class="slot-style"><slot /></div>
</template>

<script>
export default {
  props: ['bg-color', 'color', 'width', 'height'],
  computed: {
    style() {
      return `background-color: ${this.bgColor}; color: ${this.color}; width: ${this.width}; height: ${this.height};`;
    },
  },
};
</script>

<style scoped>
.slot-style {
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: center;
  font-family: Arial;
  text-align: center;
  padding: 15px;
  width: 300px;
  height: 300px;
  box-shadow: 0 3px 5px -1px rgba(0, 0, 0, 0.2),
    0 6px 10px 0 rgba(0, 0, 0, 0.14), 0 1px 18px 0 rgba(0, 0, 0, 0.12);
}
</style>
