<template>
  <div>
    <p>父级组件</p>
    <childen :name="name"
             @onUpdateName="onUpdateName"></childen>
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