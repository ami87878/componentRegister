<template>
    <div>
        <div>
            <h2>Manage Goals</h2>
            <input type="text" name="" id="" ref="goal">
            <button  @click="setGoal" >set goal</button>
            <ErrorAlert v-if="inputIsInValid">

                <h2 >input is invalid</h2>
                <p>Enter atleast a few character</p>
             

            </ErrorAlert>
           
</div>
    </div>
</template>

<script>
import ErrorAlert from './ErrorAlert.vue'
export default {


    components:{

        ErrorAlert,


    },
    name: 'ManageGoals',

    data() {
        return {
           inputIsInValid:false,
        };
    },

    mounted() {
        
    },

    methods: {


    setGoal(){

        const enteredValue=this.$refs.goal.value;

        if(enteredValue===''){

           this.inputIsInValid=true

        }


    }        
        
    },
};
</script>

<style scoped>

</style>