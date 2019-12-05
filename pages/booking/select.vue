<template>
  <div class="select-page">
    <div class="select-page-container">
      <div>
        <div class="logo"></div>

        <div style="text-align: center; font-size: 16pt;">
          Where are you want to go?
        </div>
      </div>

      <div class="map-container">
        <my-map />
      </div>

      <div>
        <div class="route-list-container">
          <nuxt-link to="/booking/select_inner">
            <div class="route-item">
              <div class="route-item-tabean">
                License Plate: AY1060
              </div>
              <div class="route-item-route">
                Rama -> Chula
              </div>
            </div>
          </nuxt-link>

          <nuxt-link to="/booking/select_inner">
            <div class="route-item">
              <div class="route-item-tabean">
                License Plate: XC1060
              </div>
              <div class="route-item-route">
                Rama -> Jim Thompson
              </div>
            </div>
          </nuxt-link>

          <nuxt-link to="/booking/select_inner">
            <div class="route-item">
              <div class="route-item-tabean">
                License Plate: AY1060
              </div>
              <div class="route-item-route">
                Rama -> Chula
              </div>
            </div>
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.select-page-container {
  display: grid;
  grid-template-rows: 50px 60% 40%;
  height: 100%;
}

.route-item {
  padding: 16px;
  margin-left: -12px;
  margin-right: -12px;
  padding-left: 24px;
  padding-right: 24px;
  background-color: darkred;
  border-bottom: 1px solid gray;

  .route-item-tabean {
    font-weight: bold;
    font-size: 16pt;
  }
}
</style>

<script>
import MyMap from '~/components/MyMap.vue'

export default {
  components: {
    MyMap
  },
  data() {
    return {}
  }
}
</script>
