<template>
  <div>
    <h1>Home</h1>
    <form action="">
      <InputField :goParentProp="propVal" @update-name="updateName"/>
      <br><button>Submit</button>
    </form>
    {{ propVal }} <br>
  </div>
</template>

<script>
import InputField from '@/components/InputField.vue';

export default {
  components: {
    InputField
  },
  data() {
    return {
      propVal: '',
    }
  },
  methods: {
    // 자식요소에서 넘겨준 값이 인자로 들어감
    updateName(case1) {
      this.propVal = case1;
    }
  }
}
</script>

<style scoped>
</style>