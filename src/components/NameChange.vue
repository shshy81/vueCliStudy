<template>
    <div>
        <p>{{name}}</p>
        <button @click="changeName">Click</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: 'cho',
        }
    },
    methods: {
        changeName() {
            this.name = 'CHO changed'
        }
    }
}
</script>