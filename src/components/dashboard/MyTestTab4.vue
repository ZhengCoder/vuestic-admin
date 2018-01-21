<template>
  <div class="charts-page">
    <div class="row my-test-tab-4">
      <div class="col-md-6">
        <vuestic-widget class="chart-widget" :headerText="'charts.verticalBarChart' | translate">
          123
        </vuestic-widget>
      </div>
      <div class="col-md-6">
        <vuestic-widget class="chart-widget" :headerText="'charts.horizontalBarChart' | translate">
          456
        </vuestic-widget>
      </div>
    </div>

    <div class="row">
      <div class="col-md-4">
        <vuestic-widget class="chart-widget" :headerText="'charts.horizontalBarChart' | translate">
          <vuestic-chart v-bind:data="horizontalBarChartData" type="horizontal-bar"></vuestic-chart>
        </vuestic-widget>
      </div>
      <div class="col-md-4">
        <vuestic-widget class="chart-widget" :headerText="'charts.horizontalBarChart' | translate">
          <vuestic-chart v-bind:data="horizontalBarChartData" type="horizontal-bar"></vuestic-chart>
        </vuestic-widget>
      </div>
      <div class="col-md-4">
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
    name: 'my-test-tab-4',

    data: function () {
      return {
        verticalBarChartData: VerticalBarChartData,
        horizontalBarChartData: HorizontalBarChartData
      }
    }
  }
</script>

<style lang="scss">
  .my-test-tab-4 {
    .widget.chart-widget {
      .widget-body {
        height: 300px;
      }
    }
  }
</style>
