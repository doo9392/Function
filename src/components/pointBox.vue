<template>
  <div :class=$style.box>
    <point v-for="(l, i) in fun" :key="i" :point="l" />
  </div>
</template>

<script>
import point from './point'

export default {
  name: 'app',
  components : {point},
  data() {
    return {
      fun: []
    }
  },
  mounted() {
    var _this = this;

    for(let k = -50; k < 50; k = k + 0.1) {
      let x = (5 * Math.cos(2 * k)) + (2 * Math.cos(3 * k));
      let y = (2 * Math.sin(3 * k)) - (5 * Math.sin(2 * k));

      setTimeout(() => {
        _this.fun.push(`translate(calc(-50% + ${x}px), calc(-50% + ${-y}px))`);
      }, 500);
    }
  }
}
</script>

<style module>
  .box {width:100%; height:100%; position:relative; margin:0 auto; transform-origin:center; transform:scale(10);}
  .box:before,
  .box:after {content:""; display:block; position:absolute; background-color:#000;}
  .box:before {width:100%; height:1px; top:50%; left:0;}
  .box:after {width:1px; height:100%; top:0; left:50%;}
  .box>span {position:absolute; width:1px; height:1px; display:block; background-color:#f00; left:50%; top:50%; transform-origin:center; border-radius:50%; z-index:1;}
</style>
