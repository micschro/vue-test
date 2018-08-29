<template>
  <div>
    <span>Parent component entity: {{entity}}</span>
    <dialog-context @entityChanged="entity = $event">
      <account-create-quote :account="entity"></account-create-quote>
    </dialog-context>
  </div>
</template>

<script>

  import AccountCreateQuote from './AccountCreateQuote.vue'
  import DialogContext from './DialogContext.vue'

  export default {
    name: 'Parent',
    components: {
      DialogContext, AccountCreateQuote
    },
    data: () => ({
      entity: null
    })
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
