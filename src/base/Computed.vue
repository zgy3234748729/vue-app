<script>
import { ref } from 'vue'
export default {
    name: 'ComputedComp',
    setup() {
        const author = ref({
            name: 'jet',
            books: [
                {
                    name: 'book1',
                    price: 100
                },
                {
                    name: 'book2',
                    price: 200
                },
                {
                    name: 'book3',
                    price: 300
                }
            ]
        })

        const authorHasBooks = computed(() => {
            return author.books.length > 0 ? '是' : '否'
        })

        // setTimeout(() => {
        //     author.value.books = []
        // }, 3000)

        return {
            author,
            authorHasBooks
        }
    }
}
</script>

<template>

    <div>作者是否出过书：{{ author.books.length > 0 ? '是' : '否' }}</div>
    <div>作者是否出过书：{{ authorHasBooks }}</div>

</template>
