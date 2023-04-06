<script>
export default{
  data(){
    return{
      title: "this is my title for Monday",
      person:{
        id: 1,
        name: 'Bill',
        img:'https://img.freepik.com/foto-gratis/rana-arbol-labios-blancos-sobre-hojas-verdes-rana-arbol-labios-blancos-litoria-infrafrenata_488145-2425.jpg?w=996&t=st=1680776367~exp=1680776967~hmac=752e9e1b13373cfb0284f2179a824cbf8d804ca78fa61b2bd3b2a5b9578b7fe3' 
      },
      msg: "Bill, uno de los integrantes de los Ranafantasmas.",
    }
  },
};
</script>

<template>
  <h3>{{ title }}</h3>
  <div :id="person.id">
    <h4>{{ person.name }}</h4>
    <img :src="person.img" :alt="person.name">
  </div>
  <h5 v-html="msg"></h5>
</template>

<style lang="css" scoped>
h3{
  color: magenta;
}
img{
  height: 300px;
  width: 400px;
}
</style>