<template>
  <div class="charts-page">
    <div class="row">
      <div class="col-md-12">
        <vuestic-widget class="chart-widget" :headerText="'charts.lineChart' | translate">
          <vuestic-chart v-bind:data="lineChartData" type="line"></vuestic-chart>
        </vuestic-widget>
      </div>
    </div>

  </div>
</template>

<script>
  import LineChartData from 'data/charts/LineChartData'

  export default {
    name: 'my-test-tab-2',

    data: function () {
      return {
        lineChartData: LineChartData
      }
    }
  }
</script>

<style lang="scss">
  .widget.chart-widget {
    .widget-body {
      height: 550px;
    }
  }
</style>
