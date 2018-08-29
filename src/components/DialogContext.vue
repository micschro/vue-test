<template>
  <div>
    <button @click="changeEntity()">Change Entity</button>
    <span>Entity: {{entity}}</span>
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: 'DialogContext',
    data: () => ({
      entity: 'FirstEntity'
    }),
    created: function () {
      this.$emit('entityChanged', this.entity)
    },
    props: {
      msg: String
    },
    methods: {
      changeEntity () {
        this.entity = ""+Date.now()
        this.$emit('entityChanged', this.entity)
      }
    }
  }
</script>

<style scoped>

</style>
