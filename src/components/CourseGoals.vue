<template>
    <ul>
 <li v-for='goal in goals' :key="goal" >
    <slot  :goalprop="goal" anotherslot="..."> </slot>

   
</li>       
    </ul>
</template>

<script>
export default {
    name: 'CourseGoals',

    data() {
        return {
            
            goals:['Finish course ','Learn Vue'],
        };
    },

    mounted() {
        
    },

    methods: {
        
    },
};
</script>

<style scoped>

</style>