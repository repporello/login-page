<template>
  <div 
    class="main-panel text-center" 
    :class="{'responsive': responsive }"
    :style="{ minWidth: minWidth }"
    >
    <div class="main-panel-title q-pb-xl">{{ title }}</div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'MainPanel',
  props: {
    minWidth: {
      type: String
    },
    title: {
      type: String
    },
    responsive: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style lang="scss">
.main-panel {
  border-radius: 20px;
  padding: 60px 65px 44px;
  -webkit-box-shadow: 0 0 30px #ddd;
        box-shadow: 0 0 30px #ddd;

  .main-panel-title {
    font-size: 40px;
    font-weight: 800;
    line-height: 1.2;
  }
}

@media (max-width: $breakpoint-tablet) {
  .main-panel {
    position: absolute;
    top: 40px;
    bottom: 40px;
    left: 40px;
    right: 40px;
    min-width: 0 !important;
  }
}

@media (max-width: $breakpoint-mobile) {
  .main-panel {
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    overflow-y: auto;
    border-radius: 0;
  }
}

</style>