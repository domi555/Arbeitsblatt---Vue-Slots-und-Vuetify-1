<template>
  <!-- <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div> -->

  <!-- <div id="app">
    <AppButton>Home</AppButton>
    <AppButton>About</AppButton>
  </div> -->

  <div id="app">
    <AppButton><img src="home.svg" /> Home</AppButton>
    <br />
    <AppButton>About <img src="info.svg" /> Me</AppButton>
  </div>
</template>

<script>
import AppButton from '@/components/AppButton.vue';

export default {};
</script>

<style scoped>
button {
  padding: 5px;
  border: 1px solid black;
  border-radius: 10px;
  text-transform: uppercase;
  width: 150px;
  height: 185px;
  background-color: white;
}
</style>
