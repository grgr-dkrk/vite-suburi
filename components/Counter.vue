<template>
  <time>{{ state.currentSec }}秒</time>
  <p aria-live="polite" aria-atomic="true">あなたは{{ state.count }}人目のお客様です</p>
  <button @click="increment">入室</button>
</template>

<script>
import { reactive } from 'vue'
import { format } from '/web_modules/date-fns.js'

export default {
  setup() {
    const state = reactive({
      count: 0,
      currentSec: format(new Date(), 'ss')
    })
    function increment() {
      state.count++
    }
    return {
      state,
      increment
    }
  }
}
</script>