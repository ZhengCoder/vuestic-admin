<template>
  <div class="charts-page">
    <div class="row">
      <div class="col-md-6">
        <vuestic-widget class="chart-widget" :headerText="'charts.verticalBarChart' | translate">
          <vuestic-chart v-bind:data="verticalBarChartData" type="vertical-bar"></vuestic-chart>
        </vuestic-widget>
      </div>
      <div class="col-md-6">
        <vuestic-widget class="chart-widget" :headerText="'charts.horizontalBarChart' | translate">
          <vuestic-chart v-bind:data="horizontalBarChartData" type="horizontal-bar"></vuestic-chart>
        </vuestic-widget>
      </div>
    </div>

  </div>
</template>

<script>
  import VerticalBarChartData from 'data/charts/VerticalBarChartData'
  import HorizontalBarChartData from 'data/charts/HorizontalBarChartData'

  export default {
    name: 'my-test-tab',

    data: function () {
      return {
        verticalBarChartData: VerticalBarChartData,
        horizontalBarChartData: HorizontalBarChartData
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
