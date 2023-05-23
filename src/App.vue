<template>
    <div class="main">
        <h1 class="text-align-center">Top FootBall Players</h1>
        <playersList :players="players" />
    </div>npm r
</template>

<script >
import playersList from './components/players-list.vue'
    export default {
        data(){
            return {
                players: []
            }
        },
        components: {playersList},
        methods: {
            async getAllPlayers() {
            
                const res = await fetch('https://football-players-backend.onrender.com/api');

                return await res.json();
            }
        },
        mounted() {
            this.getAllPlayers().then(response => {
                if(response){
                    this.players = response.data;
                }
                
            })
        }
    }
</script>
<style>
.text-align-center{
    text-align: center;
}
.main{
    padding: 10px;
}
</style>