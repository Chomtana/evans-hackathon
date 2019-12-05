<template>
  <div class="select-page">
    <div class="select-page-container">
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

          <div style="margin: 12px;">
            <div class="left-right-text">
              <div>Depature In</div>
              <div>15 : 03 Min</div>
            </div>

            <div class="left-right-text">
              <div>Traveling Time</div>
              <div>45 Min</div>
            </div>
          </div>
        </div>
      </div>

      <div class="book-now-btn-container">
        <div class="book-now-btn">
          Book Now : 30 Baht
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.select-page-container {
  display: grid;
  grid-template-rows: 60% calc(40% - 50px) 50px;
  height: calc(100% + 12px);
  margin-top: -12px;

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

.book-now-btn-container {
  text-align: right;
  margin-top: 16px;
}

.book-now-btn {
  
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
