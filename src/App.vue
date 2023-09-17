<template>
  <div>
    <TheHeader></TheHeader>
    <button v-on:click="setelectedComponent('ActiveGoal')">Active goals</button>
    <button @click="setelectedComponent('ManageGoals')">Manage goals</button>
   <active-goal  v-if="setelect==='ActiveGoal'"></active-goal>
   <manage-goals  v-if="setelect==='ManageGoals'"></manage-goals>
  </div>
</template>

<script>


import TheHeader   from "./components/TheHeader.vue";
import ActiveGoal from './components/ActiveGoal.vue'
import ManageGoals from './components/ManageGoals.vue'
export default {

  components:{

    TheHeader,
    ActiveGoal,
    ManageGoals,
    
    

  },
  data() {
    return {
      setelect:'ActiveGoal',

      activeUser: {
        name: 'Amirhossein khanmohammadi',
        description: 'Site owner and admin',
        role: 'admin',
      },
    };
  },

  methods:{

    setelectedComponent(cmp){

      this.setelect=cmp;




    }
  }
};
</script>

<style>
html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>