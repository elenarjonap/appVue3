<script>
import SingleComponent from '../components/myComponents/SingleComponent.vue';
import RawHtmlData from '../components/myComponents/RawHtmlData.vue';
import DirectiveVShow from '../components/myComponents/directives/DirectiveVShow.vue';
import DirectiveVIf from '../components/myComponents/directives/DirectiveVIf.vue';
export default { components: { SingleComponent, RawHtmlData, DirectiveVShow, DirectiveVIf } };
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
    <DirectiveVShow/>
    --------------------
    <DirectiveVIf/>
    
  </div>
</template>

<style lang="css" scoped>
h1{
  color: red;
}
</style>