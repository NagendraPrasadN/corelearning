<template>
<base-card>
    <ul v-for="item in resources" :key="item.id">
        <strong>Name:<h1>{{item.name}}</h1></strong>
    </ul>
</base-card>
</template>

<script>
export default {
    inject:['resources'],
    data(){
        return{
            
        }
    },
    computed(){
        return{
        resources:this.addResource
        }
    }
}
</script>