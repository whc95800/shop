<template>
  <h1>首页</h1>
  <p> {{ $store.state.count }} </p>
  <p> {{ store.state.count }} </p>
</template>

<script lang="ts" setup>
import {useStore} from 'vuex'

const store = useStore()

</script>

<style scoped>

</style>
