<template>
    <div class="players-container">
        <section class="player-section" v-for="player in players" :key="player.name" >
            <player :player="player" />
        </section>
    </div>
  </template>
  <script>
  import Player from './player.vue'
  export default {
    components: {Player},
    props: {
        players: Array
    }
  }
  </script>

  <style>
  .players-container{
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    grid-gap: 20px;
    padding: 15px;
  }
.player-section{
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}
</style>