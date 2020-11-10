<template>
    <div>
        <p>header</p>
        <!-- 컴포넌트 안에 별도로 html 코드를 넣고 싶을때 사용 -->
        <slot name="header"></slot>
        <p>body</p>
        <slot name="body" :param="sendData"></slot>
        <p>footer</p>
        <slot :param="sendData"></slot>
    </div>
</template>

<script>
export default {
    data() {
        return {
            sendData: 'COMPONENT DATA',
        }
    }
}
</script>