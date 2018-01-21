<template>
  <div class="dashboard">
    <!--<div class="row">-->
      <!--<div class="col-md-12">-->
        <!--<vuestic-alert type="success" :withCloseBtn="true">-->
          <!--<span class="badge badge-pill badge-success">{{'extra.alerts.success' | translate}}</span>-->
          <!--{{'extra.alerts.successMessage' | translate}}-->
          <!--<i class="fa fa-close alert-close"></i>-->
        <!--</vuestic-alert>-->
      <!--</div>-->
    <!--</div>-->

    <!--<dashboard-info-widgets></dashboard-info-widgets>-->

    <vuestic-widget class="no-padding no-v-padding full-screen">
      <vuestic-tabs :names="[$t('dashboard.dataVisualization'), $t('dashboard.usersAndMembers'),
        $t('dashboard.setupProfile'), $t('dashboard.features'),
        $t('dashboard.myTestTab1'), $t('dashboard.myTestTab2')]"
        ref="tabs">
        <div :slot="$t('dashboard.dataVisualization')">
          <data-visualisation-tab></data-visualisation-tab>
        </div>
        <div :slot="$t('dashboard.usersAndMembers')">
          <users-members-tab></users-members-tab>
        </div>
        <div :slot="$t('dashboard.setupProfile')">
          <setup-profile-tab></setup-profile-tab>
        </div>
        <div :slot="$t('dashboard.features')">
          <features-tab></features-tab>
        </div>
        <div :slot="$t('dashboard.myTestTab1')">
          <my-test-tab></my-test-tab>
        </div>
        <div :slot="$t('dashboard.myTestTab2')">
          <my-test-tab-2></my-test-tab-2>
        </div>
      </vuestic-tabs>
    </vuestic-widget>

    <!--<dashboard-bottom-widgets></dashboard-bottom-widgets>-->

  </div>
</template>

<script>
  import DashboardInfoWidgets from './DashboardInfoWidgets'
  import UsersMembersTab from './users-and-members-tab/UsersMembersTab.vue'
  import SetupProfileTab from './setup-profile-tab/SetupProfileTab.vue'
  import FeaturesTab from './features-tab/FeaturesTab.vue'
  import DataVisualisationTab from './data-visualisation-tab/DataVisualisation.vue'
  import DashboardBottomWidgets from './DashboardBottomWidgets.vue'
  import MyTestTab from './MyTestTab.vue'
  import MyTestTab2 from './MyTestTab2.vue'

  export default {
    name: 'dashboard',
    components: {
      DataVisualisationTab,
      DashboardInfoWidgets,
      UsersMembersTab,
      SetupProfileTab,
      FeaturesTab,
      DashboardBottomWidgets,
      MyTestTab,
      MyTestTab2
    }
  }
</script>

<style lang="scss" scoped>
  @import "../../sass/_variables.scss";
</style>
