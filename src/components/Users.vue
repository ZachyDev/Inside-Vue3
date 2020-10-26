<template>
  <div id="users">
    <h2>Hello {{ name }}</h2>
    <form>
      <input type="text" v-model="name" placeholder="Enter username"/><br><br>
      <input type="submit" @click.prevent="newName = name" />
      {{ newName }}
    </form>
  </div>
</template>

<script>
import { ref } from 'vue';
export default {
  name: "Users",
  setup() {
    const name = ref(null);
    const newName = ref(null);
    return {
      name,
      newName
    }
  }
}
</script>

<style scoped>
  form input {
    padding:10px;
    border-radius: 8px;
    border: 1px solid #bbb;
    outline: none;
  }
</style>