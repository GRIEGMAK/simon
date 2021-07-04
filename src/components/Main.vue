<template>
<div class="main_part">
  <game-zone></game-zone>
  <panel></panel>
</div>
</template>

<script>
import GameZone from './GameZone.vue'
import '@/styles/main.sass'
import Panel from './Panel.vue'

export default {
  name: 'Main',
  components: {
    GameZone,
    Panel
  }
}
</script>
