<template>
    <header><h1>{{title}}</h1></header>
</template>
<script>
export default {
    props:['title']
       
}
</script>
<style scoped>
header{
    margin: 0;
    align-items: center;
    text-align: center;
    width: 100%;
    display: flex;
    background-color: blueviolet;
    justify-content: center;
    height: 5rem;
}
h1{
    color: whitesmoke;
}
</style>