<template>
  <div class="tab-bar-item" @click="itemClick">
    <div class="container-item-img">
      <slot v-if="isActive" name="item-img-active"></slot>
      <slot v-else name="item-img"></slot>
    </div>
    <div :class="{ active: isActive }" :style="{color: colorActive}">
      <slot name="item-title"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "tab-bar-item",
  props: {
    path: String,
    activeColor: String
  },
  data() {
    return {};
  },
  computed: {
    isActive: {
      get() {
        return this.$route.path.indexOf(this.path) != -1;
      },
      set() {}
    },
    colorActive: {
      get() {
        return this.isActive ? this.activeColor : ""
      },
      set() {}
    }
  },
  methods: {
    itemClick() {
      console.log(this.$route.path);
      if (this.$route.path !== this.path) {
        this.isActive = !this.isActive;
        this.$router.replace(this.path);
      }
    },
  },
};
</script>

<style>

.tab-bar-item {
  flex: 1;
  text-align: center;
}

.container-item-img img{
  margin-top: 5px;
  width: 24px;
  height: 24px;
}

.active {
  color: #f44b34;
}
</style>