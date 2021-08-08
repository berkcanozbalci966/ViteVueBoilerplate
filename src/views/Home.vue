<template>
  <div>
    <h1>{{ storeTest }}</h1>
    <HelloWorld msg="test" />
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
import { useStore } from 'vuex'
import HelloWorld from '../components/HelloWorld.vue'

export default defineComponent({
  components: {
    HelloWorld,
  },
  setup() {
    const store = useStore()
    const storeTest = store.state.test

    return { storeTest }
  },
})
</script>

<style lang="scss" scoped>
h1 {
  margin-bottom: 50px !important;
}
</style>
