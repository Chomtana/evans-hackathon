<template>

  <div :class="['map-component', !noroute ? 'map-component-with-route' : 'map-component-no-route']">


  </div>
</template>

<style lang="scss" scoped>
  .map-component {
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;

    width: 100%;
    height: 100%;
  }

  .map-component-no-route {
    background-image: url("https://miro.medium.com/max/4064/1*qYUvh-EtES8dtgKiBRiLsA.png");
  }

  .map-component-with-route {
    background-image: url("https://i.stack.imgur.com/ddX9U.png");
  }
</style>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  data() {
    return {};
  },
  props: ["noroute"]
}
</script>
