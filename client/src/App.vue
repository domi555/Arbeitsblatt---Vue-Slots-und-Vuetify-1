<template
  ><div id="app">
    <!-- <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
  </div>
  -->

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
    <div style="display:flex">
      <Sheet style="margin-left:20px">
        <h3>Memo to myself</h3>
        <p>Always prepare for PLFs in time!</p>
        <img src="info.svg" width="80px" />
      </Sheet>
      <Sheet style="margin-left:20px">
        <p>INSY, SEW and Webtechnologies are our favorite subjects!</p>
        <span style="font-style: italic"
          >Starkschwitz Fiedler, Jan Schreck</span
        >
        <p>Wish i was there!</p>
        <span style="font-style: italic">E. Wahn</span>
      </Sheet>
    </div>
    <br />

    <!-- AUFGABE (1) PRO -->
    <div style="display:flex">
      <Sheet
        style="margin-left:20px"
        bg-color="#3498db"
        color="white"
        width="250"
        height="300"
      >
        <h3>Memo to myself</h3>
        <p>Always prepare for PLFs in time!</p>
        <img src="info.svg" width="80px" />
      </Sheet>
      <Sheet
        style="margin-left:20px"
        bg-color="#8e44ad"
        color="yellow"
        width="400"
        height="300"
      >
        <p>INSY, SEW and Webtechnologies are our favorite subjects!</p>
        <span style="font-style: italic"
          >Starkschwitz Fiedler, Jan Schreck</span
        >
        <p>Wish is was there!</p>
        <span style="font-style: italic">E. Wahn</span>
      </Sheet>
    </div>
    <br />

    <!-- AUFGABE (2) -->
    <AppLayout>
      <template v-slot:default>
        <AppButton><img src="home.svg" width="60" /> Home</AppButton> </template
      ><template v-slot:header>
        I was made with Vue slots!
      </template>
      <template v-slot:footer>
        By Robert Baumgartner
      </template>
    </AppLayout>
    <!-- Reihenfolge der "v-slots" ist egal.  -->
    <br />

    <!-- AUFGABE (3) -->
    <DataTable :items="desserts" :headers="headers">
      <template v-slot:header>
        <h2>Watch What You Eat!</h2>
      </template>
      <template v-slot:footer> Created 2021 by Robert Baumgartner </template>
      <template v-slot:body.append>
        <tr class="last-row">
          <td>Total</td>
          <td>{{ totalCalories }}</td>
          <td>{{ totalFat }}</td>
          <td>{{ totalCarbs }}</td>
          <td>{{ totalProtein }}</td>
          <td></td>
        </tr>
      </template>
    </DataTable>
  </div>
</template>

<script>
import AppButton from '@/components/AppButton.vue';
import Sheet from '@/components/Sheet.vue';
import AppLayout from '@/components/AppLayout.vue';
import DataTable from '@/components/DataTable.vue';

export default {
  data() {
    return {
      headers: {
        0: 'Dessert (100g serving)',
        1: 'Calories',
        2: 'Fat (g)',
        3: 'Carbs (g)',
        4: 'Protein (g)',
        5: 'Iron (%)',
      },
      desserts: [
        {
          0: 'Frozen Yogurt',
          1: '159',
          2: '6',
          3: '24',
          4: '4',
          5: '1%',
        },
        {
          0: 'Ice cream sandwich',
          1: '159',
          2: '6',
          3: '24',
          4: '4',
          5: '1%',
        },
        {
          0: 'Eclair',
          1: '159',
          2: '6',
          3: '24',
          4: '4',
          5: '1%',
        },
        {
          0: 'Cupcake',
          1: '159',
          2: '6',
          3: '24',
          4: '4',
          5: '1%',
        },
      ],
      totalCalories: 300,
      totalFat: 500,
      totalCarbs: 700,
      totalProtein: 200,
    };
  },
  components: {
    AppButton,
    Sheet,
    AppLayout,
    DataTable,
  },
};
</script>

<style>
body {
  margin: 0px;
  font-family: Arial;
  text-align: center;
}

button {
  padding: 5px;
  border: 1px solid black;
  border-radius: 10px;
  text-transform: uppercase;
  width: 150px;
  height: 185px;
  background-color: white;
}

.last-row {
  font-weight: bold;
}
</style>
