<template>

       <base-card>
            <base-button @click="setSelectedTab('stored-resourses')">Stored Resourses</base-button>
            <base-button @click="setSelectedTab('add-resourses')">Add Resourses </base-button>
        </base-card>
      <component :is=" selectedTab "></component>

</template>

<script>

import StoredResourses  from "./StoredResourses.vue";
import AddResourses from './AddResourses.vue'
export default {


    components:{

        StoredResourses, 
        AddResourses, 
    },
    name: 'TheResourses',

    data() {
        return {
            
            selectedTab:'stored-resourses'

            


        };
    },

    mounted() {
        
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