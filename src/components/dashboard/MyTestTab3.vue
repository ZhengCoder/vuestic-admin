<template>
  <div class="data-visualisation-tab dashboard-tab">
    <div class="row">
      <div class="col-md-12">
        <vuestic-widget class="col-sm-12 widget-viewport-height" headerText="Bubble Maps">
          <bubble-map v-bind:map-data="bubbleMapData"></bubble-map>
        </vuestic-widget>
      </div>
    </div>
  </div>
</template>

<script>
  import BubbleMap from '../maps/bubble-maps/BubbleMap'
  import BubbleMapData from '../../data/maps/BubbleMapData'

  export default {
    name: 'my-test-tab-3',
    components: {
      BubbleMap
    },
    data: function () {
      return {
        bubbleMapData: BubbleMapData
      }
    }
  }
</script>

<style lang="scss">

</style>
