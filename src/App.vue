<template>
  
  <!--pass array props to component-->
  <the-header title='Review Me'></the-header>
 
  
</template>

<script>
  

import TheHeader from './components/layouts/TheHeader.vue'
export default {


name:'App',


  components:{

    TheHeader,
  
    

  },
  data() {
    return {
    

      resourse: [ {
                id:'official-guide',
                title:'Official Guide',
                description:'the official Vue js documentation ',
                link:'https://vuejs.org'

            },

            {
                id:'google',
                title:'google Guide',
                description:'the google search engine ',
                link:'https://google.com'

            },
],


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