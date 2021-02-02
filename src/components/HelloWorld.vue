<template>
  <div>
    <input type="text" v-model="message">
    <span v-if="showMessage">{{ message }}</span>
    <ul v-else>
      <li v-for="item in liste" :key="item.id">{{ item.value }}</li>
    </ul>
    <button @click="leBoutton">Cacher le message</button>
  </div>

 
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'

export default defineComponent({
  name: 'Hello World',
  props: {
    msg: {
      type: String,
      required: true
    }
  },

  data () {
    return {
      message: "",
      liste: [
        { id: 1, value: "pomme" },
        { id: 2, value: "poire" },
        { id: 3, value: "banane" }
      ],
      showMessage: true,
    };
  },

  method: {
    leBoutton () {
      this.showMessage = !this.showMessage;
    }
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