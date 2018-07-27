<template>
  <span :style="`transform:${this.point}`"></span>
</template>

<script>
export default {
  name: 'point',
  props: ['point']
}
</script>
