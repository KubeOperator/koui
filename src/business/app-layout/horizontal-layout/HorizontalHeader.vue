<template>
  <div class="horizontal-header">
    <div class="header-left">
      <sidebar-toggle-button/>
    </div>
    <div class="header-right">
      <div class="navbar-item">
        <project-switch/>
      </div>
      <div class="navbar-item">
        <language-switch/>
      </div>
      <div class="navbar-item">
        <personal-setting/>
      </div>
    </div>
  </div>
</template>

<script>
  import SidebarToggleButton from "@/components/layout/sidebar/SidebarToggleButton";
  import LanguageSwitch from "@/business/app-layout/header-components/LanguageSwitch";
  import PersonalSetting from "@/business/app-layout/header-components/PersonalSetting";
  import ProjectSwitch from "../header-components/ProjectSwitch";

  export default {
    name: "HorizontalHeader",
    components: {ProjectSwitch, PersonalSetting, LanguageSwitch, SidebarToggleButton}
  }
</script>

<style lang="scss" scoped>
  @import "~@/styles/common/mixins";

  .horizontal-header {
    @include flex-row(flex-start, center);
    position: relative;
    height: 100%;

    .header-left {
      @include flex-row(flex-start, center);
      position: relative;
      height: 100%;
    }

    .header-right {
      @include flex-row(flex-end, center);
      flex: auto;
      height: 100%;

      .navbar-item {
        color: #2E2E2E;
      }

      .navbar-item + .navbar-item {
        margin-left: 20px;
      }
    }
  }
</style>
