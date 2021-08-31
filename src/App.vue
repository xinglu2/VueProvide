<template>
  <div>
    <Toolbar v-model="theme"></Toolbar>
    <button @click="changeTheme">切换{{ this.testA.theme }}</button>
  </div>
</template>

<script>
import Toolbar from './components/Toolbar.vue';

export default {
  name: 'App',
  data() {
    return {
      testA: {
        theme: 'white',
      },
    };
  },
  methods: {
    changeTheme() {
      if (this.testA.theme === 'white') {
        this.testA.theme = 'dark';
      } else {
        this.testA.theme = 'white';
      }
    },
  },
  provide() {
    return {
      test1: this.testA,
      changeTheme: this.changeTheme,
    };
  },

  components: {
    Toolbar,
  },
};
</script>
