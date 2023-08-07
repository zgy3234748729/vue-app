<script>
import { ref } from 'vue'

export default {
  name: 'StyleComp',
  setup() {
    const isTitle = ref('')
    const fontColor = ref('yellow')
    const inputColor = ref('')
    const backgroundColor = ref('')

    function changeTextColor() {
        fontColor.value = inputColor.value
    }

    return {
        isTitle,
        fontColor,
        inputColor,
        changeTextColor,
        backgroundColor
    }
  }
}
</script>

<template>
    <div :class="{title: isTitle}">123456</div>
    <button @click="isTitle = !isTitle">isTitle</button>
    <div :style="{color: fontColor, 'background-color': backgroundColor}">style</div>
    <input v-model="inputColor" />
    <button @click="changeTextColor">change</button>
    <input type="color" v-model="backgroundColor">

</template>

<style scoped>
    .title {
        color: red;
        background-color: antiquewhite;
    }
</style>

