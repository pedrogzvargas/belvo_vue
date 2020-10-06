<template>
  <div class="home">
    <Logo/>
    <HelloWorld msg="Bienvenido al cuso de Vue.js CLI"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Logo from '@/components/Logo.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Logo
  }
}
</script>
