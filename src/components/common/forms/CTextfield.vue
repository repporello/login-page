<template>
  <div class="c-textfield-container">
    <label class="text-bold">{{label}}</label>
    <q-input filled 
      class="q-pt-sm" 
      :type="isPwd ? 'password' : 'text'" 
      :dense="dense" 
      :placeholder="placeholder"
    />
    <CLink 
      class="c-link-in-input" 
      v-if="withLink" 
      :label="linkText" 
      :style="{ color: linkColor }"
    />
  </div>
</template>

<script>
import CLink from 'components/common/typography/CLink.vue';

export default {
  name: 'CTextfield',
  components: {
    CLink
  },
  data () {
    return {
      text: '',
      password: '',
      dense: true
    }
  },
  props: {
    label: {
      type: String,
      default: 'Button'
    },
    placeholder: {
      type: String,
      default: 'Button'
    },
    isPwd: {
      type: Boolean,
      default: false
    },
    withLink: {
      type: Boolean,
      default: false
    },
    linkColor: {
      type: String,
      default: '#f0c002'
    },
    linkText: {
      type: String,
      default: 'Link'
    }
  }
}
</script>

<style lang="scss">
input::placeholder {
  font-style: italic;
  font-size: 13px;
}

.c-textfield-container {
  position: relative;

  .c-link-in-input {
    position: absolute;
    right: 15px;
    bottom: 12px;
    font-size: 12px;
  }
}


</style>
