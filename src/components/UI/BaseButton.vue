<template>
<span>
<button :class="mode">
<slot></slot>
</button>  
</span>  
</template>
<script>
export default {
    props:['mode']
}
</script>
<style scoped>
span{
    margin: 5rem;
}
button{
    border-radius: 8px;
    font: bold;
    max-width: 10rem;
    background-color: teal;
    color: whitesmoke;
}
.flat{
 background-color: gray;
}
</style>