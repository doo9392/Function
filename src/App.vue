<template>
  <div :class="$style.wrap">
    <!-- <insetfun /> -->
    <pointBox />
  </div>
</template>

<script>
import insetfun from './components/insetfun'
import pointBox from './components/pointBox'

export default {
  name: 'app',
  components : {pointBox, insetfun}
}
</script>

<style module>
  *, *:before, *:after {box-sizing:border-box; margin:0; padding:0;}
  html, body {height:100%; font-family:"HelveticaNeueLTStd", "NotoSansKR", Arial, Helvetica, sans-serif; font-weight:400; overflow:hidden;}
  ul, ol, li {list-style:none;}
  a {color:#000; text-decoration:none;}
  img {border:0; display:block; width:100%;}
  table {border-collapse:collapse;}
  button {border:0; background-color:transparent; display:block;}
  select {background-color:transparent; border:0;}

  .wrap {height:100%;}
</style>
