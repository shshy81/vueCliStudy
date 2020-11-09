<template>
    <div>
        <p>{{ name }}</p>
        <button @click="changeName">Click</button>
        <hr>
        <h2>stringProp : {{ stringProp }}</h2>
        <h2 v-show="dynamicProp != null">dynamicProp : {{ dynamicProp }} </h2>
    </div>
</template>

<script>
export default {
    props: {
    // props: ['postStringProp'] // 주로 배열대신 Object 형태로 씀
        stringProp: {
            type: String,
            required: true, // 해당 컴포넌트 사용시 무조건 prop전달해야함            
        },
        dynamicProp: {
            type: String,
            required: false,
        }    
    } , 
    data() {
        return {
            name: 'cho',
        }
    },
    methods: {
        changeName() {
            this.name = 'CHO changed'
        },
    },
}
</script>