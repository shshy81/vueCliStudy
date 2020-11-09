<template>
    <div>
        <h2>부모요소에서 V-Model 사용하기</h2>
        <label for="">V-model</label>
        <input type="text" :value="value" @input="$emit('input', $event.target.value)"/>
        <!-- props사용할 요소에 :value="prop3" 이 아닌 :value="value"로 입력하고
        부모로 이벤트넘길때는 input이벤트로 $event.target.value 를 넘긴다. -->
    </div>
</template>

<script>
export default {
    props: {
        // 부모에서 v-model을 쓰면 props 이름(?)이 자동으로 value로 바뀐다.
        // 1. 기본적으로 value를 props로 컴포넌트에 전달한다.
        // 2. input 이벤트를 받아서 새로운 값을 기존 값에 할당한다.
        value: {
            type: String,
            required: true
        }
    }
}
</script>

<style scoped>
input {padding: 30px; border: 2px solid green; margin: 10px;}
</style>