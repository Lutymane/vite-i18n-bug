<script setup lang="ts">
import { ref } from 'vue'
import { useI18n } from 'vue-i18n';

defineProps<{ msg: string }>()

const count = ref(0)

const { t } = useI18n();

</script>

<i18n lang="yaml" src="/src/locale.en.yaml">
</i18n>

<!-- THIS WILL ERROR
<i18n src="/src/locale.en.yaml">
</i18n> -->

<template>
  <h1>{{ msg }}</h1>

  <p v-html="t('title')"></p>

  <button type="button" @click="count++">count is: {{ count }}</button>

  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
