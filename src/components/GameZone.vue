<template>
  <div class='game_zone'>
    <div @click='choise' class='part_1' id="1"></div>
    <div @click='choise' class='part_2' id="2"></div>
    <div @click='choise' class='part_3' id="3"></div>
    <div @click='choise' class='part_4' id="4"></div>
  </div>
</template>

<script>
import '@/styles/game_zone.sass'

export default {
  name: 'GameZone',
  props: ['choise'],
  methods: {

  }
}
</script>
