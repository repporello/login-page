<template>
  <a 
    :href="link" 
    class="text-bold" 
    :style="{ color: color }">{{ label }}
  </a>
</template>

<script>
export default {
  name: 'CTextfield',
  data () {
    return {
      text: '',
      password: '',
      dense: true
    }
  },
  props: {
    link: {
      type: String,
      default: '#'
    },
    label: {
      type: String,
      default: 'Button'
    },
    color: {
      type: String,
      default: '#414237'
    }
  }
}
</script>