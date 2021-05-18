<template>
  <div>
    <p>父级组件</p>
    <children :name="name"
             @onUpdateName="onUpdateName"></children>
  </div>
</template>
<script>
  import children from "./children";
  export default {
    components: {
      children
    },
    data() {
      return {
        name: "shuliqi"
      }
    },
    methods: {
      onUpdateName (newName) {
        this.name = newName;
      }
    }
  }
</script>
<style>
</style>