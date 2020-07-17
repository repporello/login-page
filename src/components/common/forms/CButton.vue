<template>
  <q-btn flat no-caps 
    class="full-width q-mb-sm" 
    :style="{ backgroundColor: bgColor, color: color }" 
    :label="label"
  />
</template>

<script>
export default {
  name: 'CButton',
  props: {
    bgColor: {
      type: String,
      default: '#000'
    },
    color: {
      type: String,
      default: '#fff'
    },
    label: {
      type: String,
      default: 'Button'
    }
  }
}
</script>
