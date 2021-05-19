<template>
  <div>
    <p>我是最上层组件</p>
    <B></B>
    <button @click="onUpdateParent">点击最上层组件名字</button>
  </div>
</template>
<script>
import B from "./B";
export default {
  components: {
    B
  },
  data() {
    return {
      name: "父组件的名字"
    }
  },
  provide() {
    return {
      getName: () => this.name
    }
  },
  methods: {
    onUpdateParent() {
      this.name = "最上层组件的新的名字呀"
    }
  }
}
</script>
<style>
</style>