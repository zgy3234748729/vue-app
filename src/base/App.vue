<script>
  //导入lib
  import { ref } from 'vue'

  export default {
    name: 'App', //建议给个名字，跟文件名相同
    // setup函数
    setup() {
      //创建响应式变量
      const count = ref(0)
      const obj = ref({
        skill: [1, 2, 3, 4],
        obj: {
          name: 'zgy',
          age: 20
        }
      })
      return {
        count,
        obj
      }
      
    }
  }
</script>

<template>
  <div class="title">{{JSON.stringify(obj.skill)}}</div>
</template>

<style scoped>
  .title {
    color: red;
  }
</style>
