<template>
  <div class="my-test-tab-4">
    <div class="row">
      <div class="col-md-6">
        <vuestic-widget class="chart-widget" :headerText="'charts.pieChart' | translate">
          <vuestic-chart :data="pieChartData" type="pie"></vuestic-chart>
        </vuestic-widget>
      </div>
      <div class="col-md-6">
        <vuestic-widget class="chart-widget" :headerText="'charts.donutChart' | translate">
          <vuestic-chart v-bind:data="donutChartData" type="donut"></vuestic-chart>
        </vuestic-widget>
      </div>
    </div>

    <div class="row">
      <div class="col-md-12">
        <vuestic-widget class="chart-widget" :headerText="'charts.bubbleChart' | translate">
          <vuestic-chart v-bind:data="bubbleChartData" type="bubble"></vuestic-chart>
        </vuestic-widget>
      </div>
    </div>
  </div>
</template>

<script>
  import BubbleChartData from 'data/charts/BubbleChartData'
  import PieChartData from 'data/charts/PieChartData'
  import DonutChartData from 'data/charts/DonutChartData'

  export default {
    name: 'my-test-tab-4',

    data: function () {
      return {
        bubbleChartData: BubbleChartData,
        pieChartData: PieChartData,
        donutChartData: DonutChartData
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
