<template>
  <div class="payment-page">
    <div class="information-container">
      <div style="text-align: center; font-size: 18pt; margin-bottom: 12px;">Payment</div>

      <div class="left-right-text">
        <div>Amount of seats</div>
        <div>16</div>
      </div>

      <div class="left-right-text">
        <div>License Plate</div>
        <div>AY1060</div>
      </div>

      <div class="left-right-text">
        <div>Route</div>
        <div>Rama -> Chula</div>
      </div>

    </div>

    <div class="payment-method-container">
      <v-radio-group v-model="radios">
        <v-radio label="Credit card" value="radio-1"></v-radio>
        <v-radio label="Line Pay" value="radio-2"></v-radio>
      </v-radio-group>
    </div>

    <div class="pay-bottom">
      <div class="left-right-text" style="margin-bottom: 8px; font-size: 16pt;">
        <div>Total</div>
        <div>30 Baht</div>
      </div>

      <hr />

      <nuxt-link to="/booking/payment_success">
        <div class="pay-btn-container">
          Pay Now !
        </div>
      </nuxt-link>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .information-container {
    border-bottom: 1px solid white;

    padding-bottom: 16px;
  }

  .pay-bottom {
    position: fixed;
    width: 100%;
    left: 0;
    bottom: 0;

    padding: 12px;
  }

  .pay-btn-container {
    background-color: darkred;
    font-size: 18pt;
    text-align: center;
    padding: 16px;

    margin-top: 8pt;
  }
</style>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  data() {
    return {
      radios: "radio-1"
    };
  },
}
</script>
