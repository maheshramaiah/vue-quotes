<template>
  <div>
    Quotes Added
    <div class="container">
      <div class="fill" :style="{width: count * 10 + '%'}">{{count}} / 10</div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['count']
}
</script>

<style scoped>
.container {
  position: relative;
  width: 100%;
  height: 22px;
  background: #f7f7f7;
  box-shadow: 1px -1px #bcbcbc;
}
.fill {
  position: absolute;
  background: #a6a6fc;
  width: 10%;
  text-align: center;
  overflow: hidden;
  transition: width 0.25s ease;
}
</style>
