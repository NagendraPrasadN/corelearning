<template>
<base-card>
<base-button @click="switchTab('existing-resource')" :mode="tabComponent == 'existing-resource' ? '':'flat'">Existing Resource</base-button>
<base-button @click="switchTab('add-resource')" :mode="tabComponent == 'add-resource' ? '':'flat'">Add Resource</base-button>
</base-card>
<component :is="tabComponent"></component>
</template>

<script>
import ExistingResource from './ExistingResource.vue';
import AddResource from './AddResource.vue';

export default {
  components:{ExistingResource,AddResource},
    
     provide(){
         return {
        resources:this.ExistingResourcses,
        addResource:this.addResourceFetcheddynamically
         }
    },
      data(){
        return{
            ExistingResourcses:[
                {
                    id:'1',
                    name:'Nagendra Prasad'
                }
            ],
            tabComponent:'existing-resource'
        }
    },
    methods:{
    switchTab(tab){
        this.tabComponent = tab;
    },
    addResourceFetcheddynamically(resname){
        this.ExistingResourcses.push({id:new Date().toISOString(),name:resname})
         this.tabComponent = 'existing-resource'
    }
    }
}
</script>