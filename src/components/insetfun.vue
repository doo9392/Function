<template>
  <div :class="$style.fun">
    <input type="text" v-model="funValu">
  </div>
</template>

<script>
export default {
  name: 'Insert-Function',
  data() {
    return {
      funValu : 'y=x'
    }
  },
  watch : {
    funValu(v) {
      console.log(v);
    }
  }
}
</script>

<style module>
  .fun {position:absolute; width:10vw; top:0; height:5vw; z-index:1;}
  .fun>input {display:block; width:100%; height:100%;}
</style>

