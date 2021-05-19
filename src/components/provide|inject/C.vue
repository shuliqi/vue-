<template>
  <div>
    <p>我是最底层组件</p>
    <p>最上层组件的name值：{{ name }}</p>
  </div>
</template>
<script>
export default {
  inject: ["getName"],
  computed: {
    name () {
      return this.getName();
    }
  }
}
</script>
<style>
</style>