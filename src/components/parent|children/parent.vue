<template>
  <div>
    <p>父组件</p>
    <p v-if="isShowChildrenName"> 姓名：{{ this.$children[0].name }}</p>
    <button  @click="onUpdateChildren">点击更新子组件名字</button>
    <children :parentName="name"></children>
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
        name: "父组件的名字",
        isShowChildrenName: false
     }
    },
    mounted() {
      this.isShowChildrenName = true;
    },
    methods: {
      // 修改自身的name
      uodateName(newName) {
        this.name = newName;
      },
      // 修改子组件的name
      onUpdateChildren() {
        console.log(this.$children[0]);
        //  this.$children[0].name = "新的子组件的名字"; //  直接修改子组件 data 的数据
        this.$children[0].updateName("新的子组件的名字"); // 调用父组件的方法
      }
    }
  }
</script>
<style>
</style>