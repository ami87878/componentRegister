<template>
    <base-card>
        <div class="form-control">
            <form>
                <label for="v">Title</label>
                    <input  id='title' type="text" name="title">
                
            </form>
        </div>
        
        <div class="form-control">
            <form>
                <label for="Describtion">Describtion </label>
                <textarea name="Describtion" id="Describtion"  rows="3"></textarea>
                
            </form>
        </div>
        <div class="form-control">
            <form>
                <label for="Link">Link </label>
                <input name="Link" id="Link" type="url" />
                
            </form>
        </div>

        <base-button type="submit"> Add Resourse</base-button>



    </base-card>
</template>

<script>
export default {
    name: 'AddResourses',

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

label {
  font-weight: bold;
  display: block;
  margin-bottom: 0.5rem;
}

input,
textarea {
  display: block;
  width: 100%;
  font: inherit;
  padding: 0.15rem;
  border: 1px solid #ccc;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: #3a0061;
  background-color: #f7ebff;
}

.form-control {
  margin: 1rem 0;
}


</style>