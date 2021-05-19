<template>
  <div>
    <p>子组件</p>
    <p>姓名：{{ parentName }}</p>
    <button @click="onUpdateParent">点击更新父组件名字</button>
  </div>
</template>
<script>
  export default {
    props: {
      parentName: String
    },
    data() {
      return {
        name: "子组件的名字"
      }
    },
    methods: {
      // 修改父组件的name
      onUpdateParent() {
        console.log(this.$parent);
        this.$parent.name = "新的父组件的名字"; // 直接修改父组件 data 的数据
        // this.$parent.uodateName("新的父级的组件的名字"); // 调用父组件的方法
      },
      // 修改自身的name
      updateName(newName) {
        this.name = newName;
      }
    }
  }
</script>
<style>
</style>