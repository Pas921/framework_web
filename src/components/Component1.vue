<template>
<div>
    <input type="text" v-model="message">  
    <p>{{ message }}</p>
</div>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
import Component2 from './components/Component2.vue'

export default defineComponent({
  name: 'Component1',
  props: {
    msg: {
      type: String,
      required: true
    }
  },

  components: {
      Component2
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