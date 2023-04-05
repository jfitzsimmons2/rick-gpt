<script setup lang="ts">
import { ref } from "vue";
import InputText from "primevue/inputtext";

const inputText = ref();
const response = ref();

const sendQuery = () => {
  // todo: send query to server
  alert("implement logic to send request to server:\n" + inputText.value);
  response.value = "Response from server";
};
</script>

<template>
  <div class="w-30rem m-auto">
    <h1 class="text-2xl font-bold">Query Builder</h1>
    <InputText
      v-model="inputText"
      placeholder="Enter text to be converted to a query"
      class="w-full"
      @keydown.enter="sendQuery"
    />
    <div class="mt-3">
      <pre><code>{{ response }}</code></pre>
    </div>
  </div>
</template>

<style>
hr {
  border: 0;
  height: 0;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
  border-bottom: 1px solid rgba(255, 255, 255, 0.3);
  margin: 2rem 0;
}
</style>
