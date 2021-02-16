<template>
 <the-header :title="'Resource Learning'"> </the-header>
  <the-resource></the-resource>
</template>

<script>
import TheResource from './components/Items/TheResource.vue'
export default {
  name: 'App',
  components:{TheResource}
}
</script>

<style >
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}

</style>
