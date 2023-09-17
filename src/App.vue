<template>
  <div>
    <TheHeader></TheHeader>
   <ActiveGoal></ActiveGoal>
   <ManageGoals></ManageGoals>
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
      activeUser: {
        name: 'Amirhossein khanmohammadi',
        description: 'Site owner and admin',
        role: 'admin',
      },
    };
  },
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