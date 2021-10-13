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

  <!-- <div id="app">
    <AppButton><img src="home.svg" /> Home</AppButton>
    <br />
    <AppButton>About <img src="info.svg" /> Me</AppButton>
  </div> -->

  <!-- <div id="app">
    <AppButton @click="handle"><img src="home.svg" /> Home</AppButton>
    <br />
    <AppButton>About <img src="info.svg" /> Me</AppButton>
  </div> -->

  <!-- AUFGABE (1) -->
  <!-- <div style="display:flex">
    <Sheet style="margin-left:20px">
      <h3>Memo to myself</h3>
      <p>Always prepare for PLFs in time!</p>
      <img src="info.svg" width="80px" />
    </Sheet>
    <Sheet style="margin-left:20px">
      <p>INSY, SEW and Webtechnologies are our favorite subjects!</p>
      <span style="font-style: italic">Starkschwitz Fiedler, Jan Schreck</span>
      <p>Wish i was there!</p>
      <span style="font-style: italic">E. Wahn</span>
    </Sheet>
  </div> -->

  <div style="display:flex">
    <Sheet style="margin-left:20px" bg-color="blue" color="white" width="250" height="300">
      <h3>Memo to myself</h3>
      <p>Always prepare for PLFs in time!</p>
      <img src="info.svg" width="80px" />
    </Sheet>
    <Sheet style="margin-left:20px" bg-color="purple" color="yellow" width="400" height="300">
      <p>INSY, SEW and Webtechnologies are our favorite subjects!</p>
      <span style="font-style: italic">Starkschwitz Fiedler, Jan Schreck</span>
      <p>Wish is was there!</p>
      <span style="font-style: italic">E. Wahn</span>
    </Sheet>
  </div>
</template>

<script>
// import AppButton from '@/components/AppButton.vue';
import Sheet from '@/components/Sheet.vue';

export default {
  components: {
    // AppButton,
    Sheet,
  },
};
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
