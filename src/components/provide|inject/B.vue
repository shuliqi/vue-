<template>
  <div>
    <p>我是中间层组件</p>
    <C></C>
  </div>
</template>
<script>
import C from "./C";
export default {
  components: {
    C
  },
}
</script>
<style>
</style>