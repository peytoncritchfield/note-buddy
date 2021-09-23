<template>
  <v-app id="app">
    <div>
      <img src="@/assets/Noted.png">
    </div>

        <transition name="router-anim">
        <router-view/>
        </transition>

  </v-app>
</template>

<script>


export default {
 
};
</script>

<style scoped>


#app {
  /* background-color: #149DFE; */
  background: linear-gradient(60deg, #97cbf3, #0795FF);
  text-align: center;
  min-width: 200px;
}

img {
  width: 200px;
  height: auto;
  margin-top: 10vh;
}

.router-anim-enter-active {
  animation: coming 1s;
  animation-delay: .5s;
  opacity: 0;
}

.router-anim-leave-active {
  animation: going 1s;
}

@keyframes going {
  from {
    transform: translateX(0);
  } to {
    transform: translateX(-100px);
    opacity: 0;
  }
}

@keyframes coming {
  from {
    transform: translateX(-100px);
    opacity: 0;
  } to {
    transform: translateX(0);
    opacity: 1;
  }
}
 
</style>