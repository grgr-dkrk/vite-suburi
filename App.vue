<template>
  <TheHeader />
  <Counter />
</template>

<script>
import Header from './components/Header.vue'
import Counter from './components/Counter.vue'
export default {
  components: {
    TheHeader: Header,
    Counter,
  },
}
</script>
