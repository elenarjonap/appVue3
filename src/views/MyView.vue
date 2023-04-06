<script>
import SingleComponent from '../components/myComponents/SingleComponent.vue';
import RawHtmlData from '../components/myComponents/RawHtmlData.vue';
export default { components: {SingleComponent, RawHtmlData} };
</script>

<template>
  <div>
    <h1>My Single Page from FemCoders</h1>
    <h3>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</h3>
    --------------------
    <RawHtmlData/>
    --------------------
    <SingleComponent/>
    --------------------
    
  </div>
</template>

<style lang="css" scoped>
h1{
  color: red;
}
</style>