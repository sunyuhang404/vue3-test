<template>
  <input :value="value" @input="change" />
</template>

<script>
  export default {
    props: {
      value: String,
    },
    model: {
      prop: 'value',
      event: 'changeInput'
    },
    methods: {
      change(e) {
        console.log(e.target.value);
        this.$emit('changeInput', e.target.value);
      }
    }
  }
</script>