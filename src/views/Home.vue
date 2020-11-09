<template>
  <div>
    <h1>Home</h1>
      <InputField 
        :prop1 = "propVal1" 
        @update-name = "updateName" 
        :prop2 = "propVal2" 
        @update-name2 = "propVal2 = $event.target.value"
        />
      <br><button>Submit</button>
    By Method {{ propVal1 }} <br>
    Direct Event Send {{ propVal2 }} <br>
      <!-- v-model 사용하는 컴포넌트 별도로 생성 -->
      <InputFieldVmodel v-model = "propVal3"/>
      V-model {{ propVal3 }} <br>
  </div>
</template>

<script>
import InputField from '@/components/InputField.vue';
import InputFieldVmodel from '@/components/InputFieldVmodel.vue';

export default {
  components: {
    InputField,
    InputFieldVmodel
  },
  data() {
    return {
      propVal1: '',
      propVal2: '',
      propVal3: '',
    }
  },
  methods: {
    // 자식요소에서 넘겨준 값이 인자로 들어감
    updateName(eventTargetValue) {
      this.propVal1 = eventTargetValue;
    }
  }
}
</script>

<style scoped>
</style>