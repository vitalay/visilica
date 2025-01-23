<script setup lang="ts">
import GameHeader from './components/GameHeader.vue';
import GameFigure from './components/GameFigure.vue';
import GameWrongLetters from './components/GameWrongLetters.vue';
import GameWord from './components/GameWord.vue';
import GamePopap from './components/GamePopap.vue';
import GameNotificacion from './components/GameNotificacion.vue';

</script>

<template>
<GameHeader />

    <div class="game-container">
      <GameFigure />
      <GameWrongLetters />
      <GameWord />
    </div>
       <GamePopap />
       <GameNotificacion />

</template>
