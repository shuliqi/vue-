<template>
  <div>
    <B  :name="name" 
        :age="age" 
        :sex="sex" 
        @updateName="updateName"
        :class="isActive"
        :style="isStyle"></B>
  </div>
</template>
<script>
  import B from "./B";
  export default {
    components: {
      B,
    },
    data() {
      return {
        name: "shuliqi",
        age:18, 
        sex: "女",
        isActive: "isActive",
        isStyle: "color: red"
      }
    },
    methods: {
      updateName(name) {
        this.name = name;
      }
    }
  }
</script>