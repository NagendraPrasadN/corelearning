<template>
<teleport to="body">
<base-dialog v-if="inputisInvalid" title="Invalid Input" @close="confirmError">
<template v-slot:default>
<p>Unfortnuately, Input Value is Invalid</p>
<p>Please Check all the Input entered is correct.</p>
</template>
<template #actions><base-button @click="confirmError">Okay </base-button> </template>
</base-dialog>
</teleport>

    <base-card >
     <form @submit.prevent="submitData">
         <input type="text" v-model.trim="resourceName"/>
         <base-button > Submit </base-button>
     </form>
    </base-card>
</template>
<script>
import BaseDialog from '../UI/BaseDialog.vue'
export default {
  components: { BaseDialog },
    data(){
        return{
            resourceName:'',
          inputisInvalid:false,
        }
    },
    methods:{
       submitData(){
           if(this.resourceName == '' ){
               this.inputisInvalid = true;
           }
           else{
                this.inputisInvalid = false;
           this.addResource(this.resourceName)
           }
       },
       confirmError(){
           this.inputisInvalid = false;
       }
    },
    inject:['addResource']
  
}
</script>