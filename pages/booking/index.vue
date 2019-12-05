<template>
  <div class="booking-index-page">
    <div style="text-align: center; display: flex; justify-content: center; align-items: center; font-size: 18pt; line-height: 175%;">
      OUT OF TAXI! <br />
      NO PROBLEM <br />
      USE OUR APP <br />
      AND CALL VAN! <br />
      WITH 20% DISCOUNT! <br />
    </div>

    <nuxt-link to="/booking/select">
      <div style="font-size: 20pt; padding: 18pt; background-color: darkred; text-align: center;">
        BOOK NOW!
      </div>
    </nuxt-link>
  </div>
</template>

<style lang="scss" scoped>
  .booking-index-page {
    height: 100%;

    display: grid;
    grid-template-rows: auto 100px;
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
}
</script>
