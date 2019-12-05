<template>
  <div class="payment-page">
    <div>
      <div class="information-container">
        <div style="text-align: center; font-size: 18pt; margin-bottom: 12px;" class="evan-header">
          Happy riding!
        </div>

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

      <div class="map-container" style="height: 100%;">
        <my-map />
      </div>

      <v-dialog v-model="dialog" max-width="290">
        <v-card>
          <v-card-title class="headline"
            >Payment Success</v-card-title
          >

          <v-card-text>
            Happy Riding !
          </v-card-text>

          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn color="green darken-1" text @click="dialog = false">
              OK
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </div>

    <div class="pay-bottom">
      <nuxt-link to="/identify">
        <div class="pay-btn-container">
          Check In
        </div>
      </nuxt-link>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.payment-page {
  display: grid;
  grid-template-rows: auto 100px;
}

.information-container {
  border-bottom: 1px solid white;

  padding-bottom: 16px;
}

.pay-bottom {
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
import MyMap from '~/components/MyMap.vue'

export default {
  components: {
    Logo,
    MyMap
  },
  data() {
    return {
      radios: 'radio-1',
      dialog: true
    }
  },
  asyncData() {
    console.log("adsasdadsads");

    return {};
  },
  mounted() {
    console.log("xxxxx")
  }
}
</script>
