<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h1>{{ number }}</h1>
    <button @click="incrementNumber">increment</button>
    <button @click="decrementNumber">increment</button>
  </div>
</template>

<script lang="ts">
import { ref, defineComponent } from "vue";

export default defineComponent({
  name: "Home",
  setup() {
    const number = ref(0);
    const incrementNumber = () => number.value++;
    const decrementNumber = () => number.value--;

    return { number, incrementNumber, decrementNumber };
  }
});
</script>
