<script>
import { ref } from 'vue'

export default {
    name: 'VforComp',
    setup() {

        function handleClick(e,event) {
            console.log('hhhhh')
            console.log(e,event)

            // e.target.disabled = true
        }

        const users = ref([
            {
                name: '张广园',
                age: 20,
                height: 180
            },
            {
                name: '贾依婷',
                age: 20,
                height: 170
            }
        ])

        return {
            users,
            handleClick
        }
    }
}
</script>

<template>
    <div v-for="(user, index) in users" v-bind:key="user.age">
        <div>序号{{ index + 1 }}</div>
        <div>{{ user.name }}</div>
        <div>{{ user.age }}</div>
        <div>{{ user.height }}</div>
    </div>

    <button @click="() => console.log('点击')">点击</button>
    <button @click="handleClick('msg', $event)">笑一笑</button>
</template>
