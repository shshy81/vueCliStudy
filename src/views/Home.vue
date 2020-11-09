<template>
  <div>
    <h1>{{ title }}</h1>
    <NameChange stringProp="직접 전달" :dynamicProp="postDynamicValue"/><br>
    <button @click="changeDynamicProp">changeDynamicProp</button>
  </div>
</template>

<script>
import NameChange from '@/components/NameChange.vue';

export default {
  components: {
    NameChange
  },
  data() {
    return {
      title:'This is HomePage',
      postDynamicValue: '동적 전달',
    }
  },
  methods: {
    changeDynamicProp() {
      this.postDynamicValue= '동적 수정';
    }
  }
}
</script>

<style scoped>

</style>