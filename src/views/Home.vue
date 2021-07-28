<template>
  <div class="home">
    <img alt="Paradigm logo" src="../assets/Bb_p30.svg">
    <HelloWorld msg="Welcome to Paradigm30 Chess!"/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import HelloWorld from '@/components/HelloWorld.vue' // @ is an alias to /src

export default Vue.extend({
  name: 'Home',
  components: {
    HelloWorld
  }
})
</script>
