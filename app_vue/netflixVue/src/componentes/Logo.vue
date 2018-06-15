<template>
  <div class="logo">
    <div class="logo-content">
      <div class="logo-netflix"></div>
    </div>
  </div>
</template>

<script type="text/javascript">
export default {
  props: ['titulo'],
  name: 'Logo'
}
</script>

<style scoped lang="scss">
$w: 410;
$h: 744;

.logo {
    position: relative;
    width: 100%;
    height: #{$h/2}px;
    transform: scale(0.5);
}

.logo-content {
    position: relative;
    width: 100%;
    height: 100%;
    animation: bounceIn 1s ease;
}

.logo-netflix {
    width: #{$w/2}px;
    height: #{$h/2}px;
    /* background: #ccc; */
    background-image: linear-gradient(to right, #B30000 33%, #000 33%, #000 67%, #B30000 67%, #B30000 100%);
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    &:before {
        content: '';
        width: 84px;
        height: 100%;
        position: absolute;
        background: #E80000;
        top: 0;
        left: 0;
        opacity: 1;
        transform: skewX(18deg);
        left: 29.55%;
        box-shadow: inset 0 1px 2px rgba(white, 0.2), 0 19px 38px rgba(0,0,0,0.30), 0 15px 12px rgba(0,0,0,0.22), 0 0 100px rgba(black, 0.3);
    }

    /*&:after {
        width: #{$w*1.8}px;
        height: #{$w/1.2}px;
        content: '';
        display: block;
        position: absolute;
        background: #000;
        border-radius: 100%;
        bottom: -#{$h/2.24}px;
        left: -#{$w/1.6}px;
        opacity: 1;
        transform: skewX(5deg);
    } */
}

@keyframes bounceIn {
    0%,
    100%,
    20%,
    40%,
    60%,
    80% {
        transition-timing-function: cubic-bezier(0.215, 0.610, 0.355, 1.000);
    }

    0% {
        opacity: 0;
        transform: scale3d(.3, .3, .3);
    }

    20% {
        transform: scale3d(1.1, 1.1, 1.1);
    }

    40% {
        transform: scale3d(.9, .9, .9);
    }

    60% {
        opacity: 1;
        transform: scale3d(1.03, 1.03, 1.03);
    }

    80% {
        transform: scale3d(.97, .97, .97);
    }

    100% {
        opacity: 1;
        transform: scale3d(1, 1, 1);
    }
}
</style>
