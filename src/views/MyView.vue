<script>
import SingleComponent from '../components/myComponents/SingleComponent.vue';
import RawHtmlData from '../components/myComponents/RawHtmlData.vue';
import DirectiveVShow from '../components/myComponents/directives/DirectiveVShow.vue';
import DirectiveVIf from '../components/myComponents/directives/DirectiveVIf.vue';
import DirectiveVModel from '../components/myComponents/directives/DirectiveVModel.vue';
import DirectiveVFor from '../components/myComponents/directives/DirectiveVFor.vue';
import ComputedProps from '../components/myComponents/computed-properties/ComputedProps.vue';

export default { components: { SingleComponent, RawHtmlData, DirectiveVShow, DirectiveVIf, DirectiveVModel, DirectiveVFor, ComputedProps } };
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
    --------------------
    <DirectiveVModel/>
    --------------------
    <DirectiveVFor/>
    --------------------
    <ComputedProps/>
    
  </div>
</template>

<style lang="css" scoped>
h1{
  color: red;
}
</style>