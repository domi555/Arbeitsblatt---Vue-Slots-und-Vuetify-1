<template>
  <div>
    <button v-on="$listeners"><slot /></button>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
button {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 5px;
  border: 1px solid black;
  border-radius: 10px;
  text-transform: uppercase;
  width: 150px;
  height: 185px;
  background-color: white;
}
</style>
