<script>
  import ChildComponent from './ChildComponent.vue'
  export default {
      components: { ChildComponent },
      
          data() {
              return {
                  movieTitle: 'LaRanot',
                  brandParent :"",
                  count : 0,
                  }
          },
          methods: {
              receivedBrand(data){
              this.brand = data;
              this.count++;
              }
          },
  }
</script>

<template>
    <h2>I'm your Father</h2>
    <span>Movie Title: <em>{{ movieTitle }}</em></span>
    <ChildComponent :movieTitle="movieTitle" @brand="receivedBrand" />
    <span>BRAND: <em> {{ brandParent }}</em> / {{ count }}</span>
</template>

<style lang="css" scoped>
h2{
    color: purple;
}
span{
    margin-left: 10px;
    color:blue;
}
</style>
