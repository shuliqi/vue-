<template>
  <div>
    <P>C组件的名字： {{ name }}</P>
    <button  @click="onUpdateNameOfB">修改兄弟组件B组件的名字</button>
  </div>
</template>
<script>
  import eventBus from "./eventBus";
  export default {
    data() {
      return {
        name: "我是C组件的名字"
      }
    },
    methods: {
      onUpdateNameOfB() {
        // 发送事件
        eventBus.$emit("updateNameByC", "我的 C组件，触发 B组件 的事件去修改name");
      }
    },
    mounted() {
      // 接收事件
      eventBus.$on("updateNameByB", (newName) => {
        this.name = newName;
      })
    }
  }
</script>