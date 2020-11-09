<template>
  <div>
    <h1>Home</h1>
    <form action="">
      <!-- @event이름 @click과 같이 생각하면 됨-->
      <!-- <InputField v-bind:name="name" @update-name="updateName"/> -->
      <InputField v-bind:name="name" @update-name="name = $event.target.value"/>
      <br><br><button>Submit</button>
    </form>
    {{ name }}
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
      name: '',
    }
  },
  // methods: {
  //   // 자식요소에서 넘겨준 값이 인자로 들어감
  //   updateName(name) {
  //     this.name = name;
  //   }
  // }
}
</script>

<style scoped>

</style>