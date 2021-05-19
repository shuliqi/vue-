<template>
  <div>
     <P>子组件</P>
  </div>
</template>
<script>
export default {  
  data() {
    return {
      name:"子组件的名字"
    }
  },
  methods: {
    updateName(newName) {
      this.name = newName;
    }
  }
}
</script>