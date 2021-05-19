<template>
  <div>
    <C v-bind="$attrs" v-on="$listeners"></C>
  </div>
</template>
<script>
  import C from "./C";
  export default {
    components: {
      C
    },
    props: {
      age: Number // 父级传进来的 age 值， 我们使用props接受了， 那么$attrs将不会再把这个值向下传递
    }
  }
</script>