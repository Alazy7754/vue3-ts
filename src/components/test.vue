<template>
  <div>
    <h1>{{ count }}</h1>
    <hr/>
    <button @click="handelClick">me click</button>
    <h2 class="home">312321</h2>

  </div>
</template>

<script setup lang="ts">
import {ref, computed} from 'vue'
import {useStore} from '@/store'

const store = useStore()

const count = computed(() => {
  return store.getters.getCount
})

const handelClick = () => {
  store.commit('setCount', 1)
}

</script>


<style lang="scss" scoped>
.home {
  color: rebeccapurple;
}
</style>
