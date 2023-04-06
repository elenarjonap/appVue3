<script>
import axios from 'axios'
export default {
    data(){
        return{
            chuckNorrisData:null,
        }        
    },
    created(){
        axios.get('https://api.chucknorris.io/jokes/random').then((result) => {
            this.chuckNorrisData = result.data
        })
    }
}
</script>

<template>
    <div v-if="chuckNorrisData">
        <h1>API CHUCK NORRIS</h1>
        <div class="card chuckCard" style="width: 18rem;">
            <h2>CHUCK NORRIS</h2>
            <img src="https://api.chucknorris.io/img/chucknorris_logo_coloured_small@2x.png" class="card-img-top imgChuck" alt="Chuck Norris Api Logo">
            <div class="card-body">
                <p class="card-text">JOKE: {{ chuckNorrisData.value }}</p>
                <p class="card-text">ID: {{ chuckNorrisData.id }}</p>
            </div>
        </div>
    </div>        
</template>

<style>
h1{
    color: red;
    text-align: center;
}
h2{
  color: orangered;
    text-align: center;
}
.chuckCard{
    display: flex;
    margin: auto;
    background-color:aqua;
    margin-top:10%;
    text-align: left;
    font-family: 'Courier New', Courier, monospace;
}
.imgChuck{
    width:250px;
    margin: auto;
}
</style>
