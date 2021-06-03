<template>
  <div class="tab-bar">
    <slot>
    </slot>
  </div>
</template>

<script>
export default {
  name: "tab-bar"
};
</script>

<style scoped>

.tab-bar {
  display: flex;
  align-content: center;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #F2F2F2;
  box-shadow: -1px 0px 5px gray;
}

</style>