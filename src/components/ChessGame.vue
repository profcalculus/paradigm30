<template>
    <div class="container">
  <div class="p30_chessboard">
      <div class = "row" >
      <div class='player-label'>{{playerLabel(true)}}</div>
      </div>
    <chessboard
        :orientation="orientation"
        :fen="fen"
        :onPromotion="promote" ></chessboard>
      <div class = "row" >
      <div class='player-label'>{{playerLabel(false)}}</div>
      </div>
  </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { chessboard } from '@/libs/p30-chessboard.common.js'
import '@/libs/p30-chessboard.css'

// Testing
const user = {
  screenName: 'El Nero'
}
// Testing

export default Vue.extend({
  name: 'ChessGame',
  components: {
    chessboard
  },
  props: {
    gameId: String,
    white: {
      type: String,
      default: 'Capablanca'
    },
    black: {
      type: String,
      default: 'El Nero'
    },
    fen: {
      type: String,
      default: ''
    }
  },

  methods: {
    promote () : string {
      return 'b'
    },

    playerLabel (top: boolean) : string {
      if (top) {
        return (this.orientation === 'white' ? this.black : this.white)
      } else {
        return (this.orientation === 'white' ? this.white : this.black)
      }
    }
  },
  computed: {
    orientation () : string {
      return (this.black === user.screenName ? 'black' : 'white')
    }
  }
})
</script>
<style scoped>
  .p30_chessboard {
    margin:auto;
    position:absolute;
    width:400px;
  }
