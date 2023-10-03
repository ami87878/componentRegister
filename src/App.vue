<template>
  
  <!--pass array props to component-->
  <the-header title='Review Me'></the-header>
  <TheResourses></TheResourses>
  
  
</template>

<script>
  

import TheHeader from './components/layouts/TheHeader.vue';
import TheResourses from './components/TheResourses.vue';

export default {

name:'App',


  components:{

    TheHeader,
    TheResourses, 
    

  },
  data() {
    return {
    

     

    };
  },

  methods:{

   
  }
};
</script>

<style  lang="css">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}

</style>