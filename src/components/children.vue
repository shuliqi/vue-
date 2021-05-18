<template>
  <div>
    <p>子组件</p>
    姓名：{{ name }}
    <br>
    <button @click="onUpdate">点击更新名字</button>
  </div>
</template>
<script>
  export default {
    props: {
      name: String // 父组件传下来的值
    },
    methods: {
      onUpdate () {
        // 子组件不能修改父组件传的值，只能通过$emit方式通知父组件修改值
        this.$emit("onUpdateName", "新的名字")
      }
    }
  }
</script>
<style>
</style>