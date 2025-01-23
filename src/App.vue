<script setup lang="ts">
import GameHeader from './components/GameHeader.vue';
import GameFigure from './components/GameFigure.vue';
import GameWrongLetters from './components/GameWrongLetters.vue';
import GameWord from './components/GameWord.vue';
import GamePopap from './components/GamePopap.vue';
import GameNotificacion from './components/GameNotificacion.vue';
import { ref } from 'vue';


const word = ref('василий')
const letters = ref<string[]>([])
window.addEventListener('keydown', ({key}) => {
  if (/[а-яА-ЯёЁ]/.test(key)){
    letters.value.push(key)
  }
})

</script>

<template>
 
<GameHeader />

    <div class="game-container">
      <GameFigure />
      <GameWrongLetters />
      <GameWord :word="word" />
    </div>

       <GamePopap v-if="false"/>
       <GameNotificacion />

</template>
