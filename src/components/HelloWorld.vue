<template>
  <Input v-model="input" />
  <div>{{ input }}</div>
</template>

<script>
  import Input from './Input.vue';
  export default {
    name: 'HelloWorld',
    components: {
      Input,
    },
    data() {
      return {
        input: ''
      }
    }
  }
</script>
