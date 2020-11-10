<template>
  <div class="about">
    <h1> {{ title }}</h1>
    <NameChange> 
        <!-- 부모요소에서 컴포넌트 선언 영역안에 작성한 html이 자식 컴포넌트의  slot 부분에 들어간다.
        여러개의 slot은 자식컴포넌트에서 name으로 별칭을 지정하고 
        부모요소에서 template v-slot:별칭 or #별칭 태그 안에 기재한 내용이
        자식의 해당 별칭의 slot부분으로 들어간다. -->
        <template v-slot:header>
          Header slot Contents
        </template>

        <!-- 컴포넌트에서 data를 바인딩해서 보내면 부모에서 받아서 쓸수 있다. -->
        <!-- 받아오는 변수명을 "변수명" 선언하고 사용할수 있고 data 명을 직접 적어 사용가능 -->
        <template #body="propsName">
          body slot Contents <br><br>
          <p class="red">{{ propsName.param }}</p>
        </template>

        <!-- 별칭이 없는 slot은 #default로 매핑시킨다. -->
        <template #default="{ param }">
          default Contents <br><br>
          <p class="red">{{ param }}</p>
        </template>
    </NameChange>
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

<style scoped>
.red {color : red}
</style>