<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
  <HelloWorld />
</template>

<script>
  import { computed, defineComponent, onMounted, reactive, ref } from 'vue';
  import HelloWorld from './components/HelloWorld.vue'

  export default defineComponent({
    name: 'App',
    setup(props, context) {
      const msg = ref(0);
      const input = ref('');
      const user = reactive({
        name: 'name',
        age: 28
      });
      const updateUser = () => {
        user.name = '123';
        user.age = 30
      };
      const updateMsg = () => {
        msg.value ++;
      }
      const num = computed(() => {
        return msg.value + user.age
      })
      onMounted(() => {
        msg.value = 10;
        input.value = '1231';
      })
      return { 
        msg,
        input,
        updateMsg,
        user,
        updateUser,
        num
      };
    },
    components: {
      HelloWorld
    },
  })
</script>
