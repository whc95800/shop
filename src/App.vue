<template>
  <img
    alt="Vue logo"
    src="./assets/logo.png"
  >
  <HelloWorld
    ref="helloWorld"
    msg="Hello Vue 3 + TypeScript + Vite"
    :abc="123"
    :obj="{name:'lux',age:12}"
  />
</template>

<script lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import { defineComponent, onMounted, ref } from 'vue'

export default defineComponent({
  name: 'App',
  components: {
    HelloWorld
  },
  setup () {
    const helloWorld = ref<InstanceType<typeof HelloWorld> | null>(null)
    onMounted(() => {
      console.log(helloWorld.value?.msg)
    })
    return {
      helloWorld
    }
  }
})

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
