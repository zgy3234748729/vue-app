<script>
import {ref, watch} from 'vue'

export default {
    name: 'WatchComp',
    setup() {
        const question = ref('')
        const answer = ref('')

        watch(question, async () => {
            if (question.value.indexOf('?') > -1) {
                answer.value = 'Thinking...'
                const res = await fetch()
                const result = await res.json()

            }
        })

        return {
            question,
            answer
        }
    }
}
</script>

<template>
    <input v-model="question">
    <div>{{ answer }}</div>
</template>