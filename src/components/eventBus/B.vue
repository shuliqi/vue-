<template>
  <div>
    <P>B组件名字：{{ name }}</P>
    <button  @click="onUpdateNameOfC">修改兄弟组件C组件的名字</button>
  </div>
</template>
<script>
  import eventBus from "./eventBus";
  export default {
    data() {
      return {
        name: "我是B组件的名字"
      }
    },
    methods: {
      onUpdateNameOfC() {
        // 发送事件
        eventBus.$emit("updateNameByB", "我的 B组件，触发 C组件 的事件去修改name");
      }
    },
    mounted() {
      // 接收事件
      eventBus.$on("updateNameByC", (newName) => {
        this.name = newName;
      });
    }
  }
</script>