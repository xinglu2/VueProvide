<template>
  <div :class="`button ${test1.theme}`">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "ThemeButton",
  inject:['test1','changeTheme']
};
</script>
<style>
.button {
  padding: 2px 4px;
  border-radius: 4px;
  border: 1px solid #ccc;
  display: inline-block;
}

.button.dark {
  background: #666;
  color: #fff;
}
</style>