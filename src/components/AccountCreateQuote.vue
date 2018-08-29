<template>
  <div>Child component account value: {{account}}</div>
</template>

<script>
export default {
  name: 'AccountCreateQuote',
  props: {
    account: String
  }
}
</script>

<style scoped>

</style>
