<template>

       <base-card>
            <base-button @click="setSelectedTab('stored-resourses')">Stored Resourses</base-button>
            <base-button @click="setSelectedTab('add-resourses')">Add Resourses </base-button>
        </base-card>
      <component :is="selectedTab"></component>

</template>

<script>

import StoredResourses  from "./StoredResourses.vue";
import AddResourses from './AddResourses.vue'
export default {

    name:'TheResourses',
    components:{

        StoredResourses, 
        AddResourses, 
    },
   

    data() {
        return {
            
            selectedTab:'stored-resourses',

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

    mounted() {
        
    },



    provide(){

        return{

            resourses:this.resourse,


        };


    },
    methods: {
        
        setSelectedTab(tab){

             this.selectedTab=tab;

        }


    },
};
</script>

<style scoped>

</style>