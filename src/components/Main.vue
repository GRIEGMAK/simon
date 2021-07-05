<template>
<div class="main_part">
  <game-zone :choise="choise"></game-zone>
  <panel :round='round' :complication='complication' :start='start' :start_game='start_game'></panel>
</div>
</template>

<script>
import GameZone from './GameZone.vue'
import '@/styles/main.sass'
import Panel from './Panel.vue'
import genRandom from '@/utilits/genRandom.js'
import play from '../utilits/play'

export default {
  name: 'Main',
  components: {
    GameZone,
    Panel
  },
  data() {
    return{
      round: 0,
      complication: '1000',
      array: [],
      start_game: true,
      choise(event) {
        const value = event.target.id;
        switch (value) {
          case "1":
            new Audio(require("../sounds/1.mp3")).play();
            break;
          case "2":
            new Audio(require("../sounds/2.mp3")).play();
            break;
          case "3":
            new Audio(require("../sounds/3.mp3")).play();
            break;
          case "4":
            new Audio(require("../sounds/4.mp3")).play();
            break;
        }
      }
    }
  },
  methods: {
    start() {
        this.round++
        this.array += genRandom()
        console.log(this.array, this.round)
        play()
    },
  }
}
</script>
