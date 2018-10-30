<template>
  <div class="header">
    <div class="w v-center inner-hd">
      <slot />
    </div>
  </div>
</template>

<script>
  export default {

  }
</script>
<style lang="less" scoped>
  .header {
    position: relative;
    z-index: 1;
    height: 120px;
    background-color: @mainColor;
    color: #fff;
  }

  .inner-hd {
    height: 100%;
  }
</style>
