<script>
import { ref, onMounted, onUpdated, onUnmounted } from 'vue'

export default {
  name: 'TimeComp',
  setup() {
    // 回调函数既可以传同步，也可以传递异步的
    onMounted(() => {
      // 做数据初始化
      console.log('onMounted')
    })
    onUpdated(() => {
      console.log('onUpdated')
    })
    onUnmounted(() => {
      // 监听时间函数的销毁
      
      console.log('onUnmounted')
    })

    function sleep(time) {}

    const time = ref(0)
  }
}
</script>

<template>
  <div id="time">{{ time }}</div>
</template>
