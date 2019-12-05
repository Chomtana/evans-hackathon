<template>
  <div class="arrive-in-page">
    <div class="map-container" style="height: 100%;">
      <my-map />
    </div>

    <div class="arrive-in-container">
      <div style="font-size: 18pt;">
        Arrive In
      </div>
      <div style="font-size: 20pt;">
        15 : 30 min
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .arrive-in-page {
    display: grid;
    grid-template-rows: 75% 25%;
  }

  .information-container {
    border-bottom: 1px solid white;

    padding-bottom: 16px;
  }

  .arrive-in-container {
    text-align: center;
    margin-top: 16px;
  }
</style>

<script>
import Logo from '~/components/Logo.vue'
import MyMap from '~/components/MyMap.vue'

export default {
  components: {
    Logo, MyMap
  },
  data() {
    return {
      radios: "radio-1"
    };
  },
}
</script>
