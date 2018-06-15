<template>
<div class="slider">
  <h3>{{titulo}}</h3>
  <span v-on:mouseover="scrollEsquerda()" v-on:mouseout="clearScroll()" class="handle handlePrev active">
      <i class="fa fa-caret-left" aria-hidden="true"></i>
    </span>

  <div ref="scroller" class="row">
    <div class="row__inner">

      <filme></filme>

      <div class="gui-card">
        <div class="gui-card__media">
          <img class="gui-card__img" src="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700" alt="" />
        </div>
        <div class="gui-card__details">
          <div class="gui-card__title">
            Assassin's Creed
          </div>
        </div>
      </div>

    </div>
  </div>

  <span v-on:mouseover="scrollDireita()" v-on:mouseout="clearScroll()" class="handle handleNext active">
    <i class="fa fa-caret-right" aria-hidden="true"></i>
  </span>

</div>
</template>

<script type="text/javascript">
import filme from './Filme.vue';

export default {
  props: ['titulo'],
  components: {
    Filme
  },
  data() {
    return {
      intervalo: null
    }
  },
  methods: {
    scrollDireita: function() {
      this.intervalo = setInterval(() => {
        this.$refs.scroller.scrollLeft += 2
      }, 5);
    },
    scrollEsquerda: function() {
      this.intervalo = setInterval(() => {
        this.$refs.scroller.scrollLeft -= 1
      }, 5);
    },
    clearScroll: function() {
      clearInterval(this.intervalo);
    }
  }
}
</script>

<style lang="scss"></style>
