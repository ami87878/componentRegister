<template>
    <div>
        <ul>
    <learen-resourse v-for="item in resourses"
     :key="item.id"
     :title="item.title"
     :id="item.id"
     :description="item.description"
     :link="item.link"
     > <!--component that render list  from props that come from App-->

    </learen-resourse>

  </ul>
    </div>
</template>

<script>

import LearenResourse from "./LearenResourse.vue";

export default {
    
    name: 'StoredResourses',

    components:{

      LearenResourse,
     

    },
    inject:['resourses'],// props  that come from App

    data() {
        return {
            
        };
    },

    mounted() {
        
    },

    methods: {
        
    },
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>