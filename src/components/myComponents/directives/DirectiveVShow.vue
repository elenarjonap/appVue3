<script>
export default {
  data(){
    return{
      isShowing: true,
    }
  },
  methods:{
    /* function changeState() */
    changeState(){
      if (this.isShowing){
        this.isShowing = false;
        return 
      }
      this.isShowing = true;
    }
  },
};
</script>

<template>
  <div>
    <h3>V Show directive</h3>
    <button v-on:click="changeState">
      <spam v-show="isShowing">One upon a time...</spam>
    </button>
  </div>
</template>

<style lang="css" scoped>
</style>