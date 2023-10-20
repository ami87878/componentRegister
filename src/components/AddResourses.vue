<template>
    <base-dialog v-if="inputIsInvalid" title="Invalid Input">
    
    <template #default >
      
      
      <section>
       
          <p>at least write something  in empty field</p>
          <p>please check your input  and make sure you enter at leat  one input </p>
  
      
      <base-button @click="confirmError">Okay</base-button>
    
    </section>
      
    </template>
    
    
  
      

  

        
        
        
       


</base-dialog>
    <base-card>
    <form  @submit.prevent="submitData">
        <div class="form-control" >

                <label for="title">Title</label>

                    <input  id='title' type="text" name="title" ref="titleInput">
                
                </div>
                
                <div class="form-control">
            
                        <label for="Describtion">Describtion </label>
                        <textarea name="Describtion" id="Describtion"  rows="3" ref="DescribtionInput" ></textarea>
                        
            
                  </div>

        <div class="form-control">
            
                <label for="Link">Link </label>
                <input name="Link" id="Link" type="url"  ref="LinkInput"/>
                
        
        </div>

                 <div>
                        <base-button type="submit"> Add Resourse</base-button>
                 </div>
    </form>



    </base-card>
</template>

<script>

export default {


    name: 'AddResourses',

    

    inject:['addResource'],

    data() {
        return {
          
          inputIsInvalid:false,
        };
    },

    mounted() {
        
    },

    methods: {

        submitData(){

            const titleDta=this.$refs.titleInput.value;
            const DescribtionData=this.$refs.DescribtionInput.value;
            const Linkdata=this.$refs.LinkInput.value;

            if(titleDta.trim()==='' || DescribtionData.trim()==='' || Linkdata.trim()===''){

              this.inputIsInvalid=true;

                return;

            }


            this.addResource(titleDta,DescribtionData,Linkdata);

        },

        confirmError(){


          this.inputIsInvalid=false;
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
