<template>
  <div>
     <P>父组件</P>
     <p v-if="isShowChildrenName">名字：{{this.$refs.childrenRef.name}}</p>
      <button  @click="onUpdateChildren">点击更新子组件名字</button>
     <children ref="childrenRef"></children>

  </div>
</template>
<script>
import children from "./children"
export default {  
  components: {
    children
  },
  data() {
    return {
      isShowChildrenName: false
    }
  },
  mounted() {
    this.isShowChildrenName = true;
  },
  methods: {
    onUpdateChildren() {
      // this.$refs.childrenRef.updateName("新的组件的名字"); // 调用子组件的方法
      this.$refs.childrenRef.name = "新的组件的名字"; // 调用子组件的data
    }
  }
}
</script>