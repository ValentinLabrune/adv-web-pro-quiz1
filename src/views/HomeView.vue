<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/Logo.svg">
    <HeaderMenu/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HeaderMenu from '@/components/HeaderMenu.vue'
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HeaderMenu,
    HelloWorld
  }
}
</script>
