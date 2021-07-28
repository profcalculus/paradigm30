<template>
  <div class="p30_chessboard">
    <h1>This is the Paradigm30 chessboard</h1>
    <ChessGame :gameId = 'unknown'></ChessGame>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import ChessGame from '@/components/ChessGame.vue'
export default Vue.extend({
  name: 'ChessRoom',
  components: {
    ChessGame
  }
})
</script>
<style scoped>
  .p30_chessboard {
    margin:auto;
    position:absolute;
    width:400px;
  }
