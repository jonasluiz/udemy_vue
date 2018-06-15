<template>
  <div class="gui-card">
    <div class="gui-card__media">
      <img class="gui-card__img" v-bind:src="imagem" alt="" />
    </div>
    <div class="gui-card__details">
      <div class="gui-card__title">
        {{titulo}}
      </div>
    </div>
  </div>
</template>

<script type="text/javascript">
  export default{
    props: ['titulo', 'imagem']
    // https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700
  }
</script>

<style lang="scss">

</style>
