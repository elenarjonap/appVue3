<script>
import axios from 'axios'
export default {
    data(){
        return{
            pokemonData:null,
        }        
    },
    created(){
        axios.get('https://pokeapi.co/api/v2/pokemon/pikachu').then((result) => {
            this.pokemonData = result.data
        })
    }
}
</script>

<template>
    <div v-if="pokemonData">
        <h1>API POKEMON</h1>

        <div class="card pokemonCard" style="width: 18rem;">
            <h5 class="card-title">Name: {{ pokemonData.name }}</h5>
            <img class="imgPokemon card-img-top" :src="pokemonData.sprites.other.dream_world.front_default" alt='{{ pokemonData.name }}'>
            <div class="card-body">
                <p class="card-text">HP: {{ pokemonData.stats[0].base_stat }}</p>
                <p>Speed: {{ pokemonData.stats[1].base_stat }}</p>
                <p>Attack: {{ pokemonData.stats[3].base_stat }}</p>
                <p>Weight: {{ pokemonData.weight }}</p>
                <p>Height: {{ pokemonData.height }}</p>
            </div>
        </div>
    </div>
</template>

<style>
.pokemonCard{
    display: flex;
    margin: auto;
    margin-top:10%;
    background-color: grey;
    text-align: center;
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    color: white;
}
.imgPokemon{
    width:150px;
    margin: auto;
}
</style>
