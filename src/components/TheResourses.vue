<template>

    <base-card>
             <base-button @click="setSelectedTab('stored-resourses')" :mode="storeResButtonMode">Stored Resourses</base-button>
             <base-button @click="setSelectedTab('add-resourses')" :mode="addResButtonMode">Add Resourses </base-button>
     </base-card>
     <keep-alive>
         <component :is="selectedTab"></component>
         
     </keep-alive>

</template>

<script>

import StoredResourses  from "./StoredResourses.vue";
import AddResourses from "./AddResourses.vue"
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

 computed:{

     storeResButtonMode(){

        
         return this.selectedTab==='stored-resourses' ? null : 'flat';
         

     },

     addResButtonMode(){

         return this.selectedTab==='add-resourses' ?  null :'flat';

     }
     
 },



 provide(){

     return{

         resourses:this.resourse,
         addResource:this.addResource,
         removeResourse:this.removeResourse,

     };


 },

 methods: {
     
     setSelectedTab(tab){

          this.selectedTab=tab;

     },


    addResource(title,description,url){
     
  const newResource={

         id:new Date().toISOString(),
         title:title,
         description:description,
         link:url,

          }

          this.resourse.unshift(newResource),
          this.selectedTab='stored-resourses'
     },

     removeResourse(resId){

        const resIndex=this.resourse.findIndex(item=>item.id===resId);
        this.resourse.splice(resIndex,1);
        


   }

 },
};
</script>

<style scoped>

</style>