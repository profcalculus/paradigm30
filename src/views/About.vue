<template>
  <div class="about">
    <h1>This is an about page</h1>
    <chessboard></chessboard>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { chessboard } from '@/libs/p30-chessboard.common.js'
import '@/libs/p30-chessboard.css'
export default Vue.extend({
  name: 'About',
  components: {
    chessboard
  }
})
</script>
