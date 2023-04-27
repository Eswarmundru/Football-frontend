<template>
    <article class="player-card">
        <header>
            <h2 class="name">{{ player.name }}</h2>
        </header>    
        <!-- <img :src="player.image" /> -->
        <div class="content">
            <p>Country: {{ player.country }}</p>
            <p>Age: {{ player.age }}</p>
            <p>Matches: {{ player.matches }}</p>
            <p>Goals: {{ player.goals }}</p>
            <p>Clubs: {{ player.clubs }}</p>
        </div>  
    </article>

  </template>
  <script>
  export default {
      props: {
          player: Object
      }
  }
  </script>
  <style>

.player-card {
    text-align: center;
    border-radius: 8px;
    padding: 10px;
}

.player-card img {
  width: 150px;
    height: 150px;
    border-radius: 50%;
    margin: auto;
}
.name{
  padding-bottom: 10px;
  font-weight:bold;
}
.content{
  padding-top: 15px;
  line-height: 26px;
}
p{
  font-weight: bold;
}
</style>