<template>
  <div class="select-page">
    <div class="container">
      <div>
        <div class="logo"></div>

        <div>
          Where are you want to go
        </div>
      </div>

      <div class="map-container">
        <my-map />
      </div>

      <div>
        <div class="route-list-container">
          <div class="route-item">
            <div class="route-item-tabean">
              License Plate: AY1060
            </div>
            <div class="route-item-route">
              Rama -> Chula
            </div>
          </div>

          <div class="route-item">
            <div class="route-item-tabean">
              License Plate: XC1060
            </div>
            <div class="route-item-route">
              Rama -> Jim Thompson
            </div>
          </div>

          <div class="route-item">
            <div class="route-item-tabean">
              License Plate: AY1060
            </div>
            <div class="route-item-route">
              Rama -> Chula
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: grid;
  grid-template-rows: 200px 60% 40%;
}

.route-item {
  padding: 8px;
  margin-left: -24px;
  margin-right: -24px;
  padding-left: 24px;
  padding-right: 24px;
  background-color: darkred;
  border-bottom: 1px solid gray;
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
