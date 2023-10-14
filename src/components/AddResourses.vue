<template>
    <base-card>
        <div class="form-control" @submit.prevent="submitData">
            <form>
                <label for="v">Title</label>
                    <input  id='title' type="text" name="title" ref="titleInput" >
                
            </form>
        </div>
        
        <div class="form-control">
            <form>
                <label for="Describtion">Describtion </label>
                <textarea name="Describtion" id="Describtion"  rows="3" ref="DescribtionInput" ></textarea>
                
            </form>
        </div>
        <div class="form-control">
            <form>
                <label for="Link">Link </label>
                <input name="Link" id="Link" type="url"  ref="LinkInput"/>
                
            </form>
        </div>

        <base-button type="submit"> Add Resourse</base-button>



    </base-card>
</template>

<script>
export default {
    name: 'AddResourses',

    inject:['addResourceTochild'],
    data() {
        return {
          
        
        };
    },

    mounted() {
        
    },

    methods: {

        submitData(){

            const titleDta=this.$refs.titleInput.value;
            const DescribtionData=this.$refs.DescribtionInput.value;
            const Linkdata=this.$refs.LinkInput.value;
            
            this.addResourceTochild(titleDta,DescribtionData,Linkdata),

        }
        
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