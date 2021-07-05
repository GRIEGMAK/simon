<template>
<div>
    <div class='header_panel'>
      Раунд: {{round}} 
    </div>
    <div>
      <button @click='start'>
        Старт
      </button>
    </div>
    <div>
      <p class="sorry" v-if="start_game === 'false'">
        Sorry, you lost after {{ round }} rounds!
      </p>
    </div>
    <div>
      <div>
        <input type='radio' name='mode' value='1500' id="lite" v-model="complication"/>
        <label for="lite">Легкий</label>
      </div>

      <div>
        <input type='radio' name='mode' value='1000' id="middle" v-model="complication"/>
        <label for="middle">Средний</label>
      </div>

      <div>
        <input type='radio' name='mode' value='400' id="hard" v-model="complication"/>
        <label for="hard">Сложный</label>
      </div>
    </div>
</div>
</template>

<script>
import '@/styles/panel.sass'

export default {
  name: 'Panel',
  props: ['round', 'complication', 'start', 'start_game']
}
</script>
