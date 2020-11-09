<template>
  <div>
    <h1>{{ title }}</h1>
    <NameChange/>
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
    }
  }
}
</script>

<style scoped>

</style>