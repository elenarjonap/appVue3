<script>
  export default {
      props: {
      movieTitle: String,
      },
      data() {
          return {
          brandChild: 'DC Comics',
          }
      },
      methods:{
          sendBrand(){
              this.$emit('brand', this.brandChild)
          }
      }
  }
</script>

<template>
    <h2>Hijita</h2>
    <h3>Movie Title received From Father: <em>{{ movieTitle }}</em>ita bonica</h3>
    <button @click="sendBrand">sendBrand</button>
</template>

<style lang="css" scoped>
h2{
    color: purple;
}
h3{
    color: green;
}
button{
    color:white;
    background-color:violet;
    border-color: none;
    border-radius: 10px;
    width: 150px;
}
span{
    margin-left: 10px;
    color:blue;
}
</style>