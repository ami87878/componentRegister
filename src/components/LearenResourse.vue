<template>
    
   <li>
    
        <base-card> <!-- base card that  have slot  -->
        <header>
                <h3>{{ title }}</h3>
                <base-button mode="flat" @click="removeResourse(id)">Delete</base-button>
        </header>
                <p>{{ description }}</p>
                <nav>
                    <a v-bind:href="link">View Resourse link</a>
                </nav>
        </base-card>
            
        
    
   </li>

</template>

<script>
 


 
export default {
   
    name: 'LeaenResourse',
    
    // components:{
    //     BaseCard,
    // },

    props:['id','link','title','description'],

    inject:['removeResourse'],

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

li {
  margin: auto;
  max-width: 40rem;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h3 {
  font-size: 1.25rem;
  margin: 0.5rem 0;
}

p {
  margin: 0.5rem 0;
}

a {
  text-decoration: none;
  color: #ce5c00;
}

a:hover,
a:active {
  color: #c89300;
}

</style>