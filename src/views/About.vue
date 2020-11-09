<template>
  <div class="about">
    <h1> {{ title }}</h1>
    <NameChange stringProp="About 직접전달"/>
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
      title : 'This is an about page'
    }
  }
}
</script>
