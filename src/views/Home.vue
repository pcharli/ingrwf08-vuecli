<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Hello ingwf-08"/>
    <input type="text" class="sortie" v-model="essai2">
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  data() {
    return {
      essai: "Pierre"
    }
  },
  computed: {
    essai2() {
      return "Hello" + this.essai
    }
  }
}
</script>
