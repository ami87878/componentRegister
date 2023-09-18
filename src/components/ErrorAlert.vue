<template>
    <div>
        <dialog open>
            <slot></slot> <!--content  is flexible-->
        </dialog>
    </div>
</template>

<script>
export default {
    name: 'ErrorAlert',

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

dialog{


    position: fixed;
    top: 20vh;
    left: 30%;
    width: 40%;
    background-color: white;
    box-shadow: 0 2px 8px rgb(34, 163, 185);
    padding: 1rem;
    margin: 0;
    border-radius: 0.4rem;
}

</style>