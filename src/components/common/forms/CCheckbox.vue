<template>
  <div>
    <q-checkbox 
      class="text-bold"
      color="grey"
      size="xs"
      name="stay_signed_in"
      v-model="staySignedIn"
      :label="label"
    />
  </div>
</template>

<script>


export default {
  name: 'CCheckbox',
  data () {
    return {
      staySignedIn: false
    }
  },
  props: {
    label: {
      type: String,
      default: 'Label'
    }
  }
}
</script>

<style lang="scss">

</style>
