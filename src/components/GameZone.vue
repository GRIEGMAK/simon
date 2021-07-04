<template>
  <div class='game_zone'>
    <div @click='clickPart(1)' class='part_1'></div>
    <div @click='clickPart(2)' class='part_2'></div>
    <div @click='clickPart(3)' class='part_3'></div>
    <div @click='clickPart(4)' class='part_4'></div>
  </div>
</template>

<script>
import '@/styles/game_zone.sass'

export default {
  name: 'GameZone',
  methods: {
    clickPart(part_index) {
      console.log(part_index)
    }
  }
}
</script>
