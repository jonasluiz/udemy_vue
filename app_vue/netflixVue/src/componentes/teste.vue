<template>
  <h1>{{titulo}}</h1>
</template>

<script type="text/javascript">
  export default{
    name: 'teste',
    props: ['titulo']
  }
</script>

<style lang="scss">
  h1{
    color: red;
  }
</style>
