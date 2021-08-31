<template>
  <div>
    <div :class="`toolbar ${test1.theme}`">
      <theme-button @click="changeTheme">确定{{ this.test1.theme }}</theme-button>
    </div>
  </div>
</template>
<script>
import ThemeButton from './ThemeButton.vue';

export default {
  components: {ThemeButton},
  name: 'Toolbar',
  inject: ['test1', 'changeTheme'],
};
</script>
<style>
.toolbar {
  border: 1px solid #333;
  color: #333;
  padding: 10px;
}

.toolbar.dark {
  background: #333;
  color: #fff;
}


</style>