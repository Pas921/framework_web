<template>
<div>
    <input type="text" v-model="message">
</div>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
import Component3 from './components/Component3.vue'

export default defineComponent({
  name: 'Component2',
  props: {
    msg: {
      type: String,
      required: true
    }
  },

  object: {

  },

  components: {
      Component3
  },

  setup: () => {
    const count = ref(0)
    return { count }
  }
})
</script>

<style scoped>
a {
  color: #42b983;
}
</style>