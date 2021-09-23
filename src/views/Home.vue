<template>
  <div class="main container">

   

    <h1>simply organized</h1>

    <v-btn class="button"><router-link to="/login" style="text-decoration: none"> Login </router-link></v-btn>
    <router-view/>

  </div>
</template>

<script>

  export default {

  }
</script>

<style scoped>

.main-container {
 
}

h1 {
  color:white;
  margin-top: 100px;
}

.button {
  width: 100px;
  margin-top: 80px;
}



</style>
