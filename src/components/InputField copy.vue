<template>
    <div>
        <!-- 자식요소의 input value를 부모요소로 올리는것 -->
        <!-- v-model="goParentProp" 
        부모에서 쓸때는 v-model 로 써도 되지만 컴포넌트로 빠지면서
        자식요소에서 props를 변경하면 안되서 input 요소의 value에 name 을 바인딩-->
        <h2>부모요소로 데이터 보내기 Emit</h2>
        <label for="">By Method</label>
        <input type="text" :value="goParentProp" @input="updateName"/>        
    </div>
</template>

<script>
export default {
    props: {
        goParentProp : {
            type: String,
            required: true
        },
    },
    methods: {
        updateName(e) {
            // console.log(e.target.value);
            // $emit(부모에서 사용할 이벤트 이름, 넘길값);
            this.$emit('update-name', e.target.value);
        }
    }
}
</script>

<style scoped>
input {padding: 30px; border: 2px solid green; margin: 10px;}
</style>