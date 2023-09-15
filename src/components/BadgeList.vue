<template>
  <section>
    <BaseCard>
     <template v-slot:headerslot>
    
    <h2>Available Badges</h2>

  </template>

  <template v-slot:default>
    

    <ul>
      <li>
        <base-badge type="admin" caption="admin"></base-badge>
      </li>
      <li>
        <base-badge type="author" caption="author"></base-badge>
      </li>
    </ul>
  </template>
  </BaseCard>
  </section>
</template>

<script>

import BaseCard from './BaseCard.vue';

export default{

  name:'BadgeList',





  components:{

    BaseCard,


  },
data() {
  return {
    property: 'value',
  };
},

methods:{


}

}




</script>

<style scoped>



section h2 {
  margin: 0.5rem 0;
  color: #5f5858;
}
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
}

li {
  margin-right: 1rem;
}
</style>