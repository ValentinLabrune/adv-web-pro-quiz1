<template>
  <div class="about">
    <HeaderMenu/>
    <h1>This is an about page</h1>
  </div>
</template>

<script>
import HeaderMenu from '@/components/HeaderMenu.vue'

export default {
  name: 'HomeView',
  components: {
    HeaderMenu
  }
}
</script>

<style>
.home{
  background-color: #F9D9AA;
}
</style>
