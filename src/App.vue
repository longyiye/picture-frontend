<template>
  <div id="app">
    <BasicLayout />
  </div>
</template>

<script setup lang="ts">
import BasicLayout from '@/layouts/BasicLayout.vue'
import { testUsingGet } from '@/api/testController'
import { useLoginUserStore } from '@/stores/useLoginUserStore'

const loginUserStore = useLoginUserStore()
loginUserStore.fetchLoginUser()

testUsingGet().then((res) => {
  console.log(res)
})
</script>

<style>
#app {
}
</style>
