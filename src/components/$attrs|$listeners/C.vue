<template>
  <div>
    <p>名字：{{ name }}</p>
    
    <button  @click="onUpdateName">点击更新最上层的name值</button>
  </div>
</template>
<script>
  export default {
    props: {
      name,
    },
    created() {
      console.log("this.$attrs:",this.$attrs);
      console.log("this.$listeners:",this.$listeners);
      
    },
    methods: {
      onUpdateName() {
        this.$listeners.updateName("新的名字")
      }
    }
  }
</script>