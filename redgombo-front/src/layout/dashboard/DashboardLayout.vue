<template>
  <div class="wrapper">
    <side-bar>
      <template slot="links">
        <!-- <sidebar-link to="/dashboard" name="Dashboard" icon="ti-panel" /> -->
        <sidebar-link to="/index" name="Profile" />
        <!-- <sidebar-link to="/maps" name="Map" icon="ti-map" /> -->

        <!-- <sidebar-link to="/testPage2" name="Test Page2" />y

        <sidebar-link to="/testPage3" name="Test Page3" /> -->
        <!-- <sidebar-link
          to="/table-list"
          name="Table List"
          icon="ti-view-list-alt"
        />
        <sidebar-link to="/typography" name="Typography" icon="ti-text" />
        <sidebar-link to="/icons" name="Icons" icon="ti-pencil-alt2" />
        <sidebar-link to="/maps" name="Map" icon="ti-map" />
        <sidebar-link to="/notifications" name="Notifications" icon="ti-bell" /> -->
      </template>
      <mobile-menu>
        <li class="nav-item">
            <a href = "https://medium.com/@jc3wrld999" class="nav-link">
              <i class="ti-ink-pen"></i>
              <p>Medium</p>
            </a>
          </li>

          <!-- <drop-down
            class="nav-item"
            title="5 Notifications"
            title-classes="nav-link"
            icon="ti-bell"
          >
            <a class="dropdown-item" href="#">Notification 1</a>
            <a class="dropdown-item" href="#">Notification 2</a>
            <a class="dropdown-item" href="#">Notification 3</a>
            <a class="dropdown-item" href="#">Notification 4</a>
            <a class="dropdown-item" href="#">Another notification</a>
          </drop-down> -->
          <li class="nav-item">
            <a href="https://github.com/jc3wrld999" class="nav-link">
              <i class="ti-github"></i>
              <p>GitHub</p>
            </a>
          </li>
        <li class="divider"></li>
      </mobile-menu>
    </side-bar>
    <div class="main-panel">
      <top-navbar></top-navbar>

      <dashboard-content @click.native="toggleSidebar"> </dashboard-content>

      <content-footer></content-footer>
    </div>
  </div>
</template>
<style lang="scss"></style>
<script>
import TopNavbar from "./TopNavbar.vue";
import ContentFooter from "./ContentFooter.vue";
import DashboardContent from "./Content.vue";
import MobileMenu from "./MobileMenu";
export default {
  components: {
    TopNavbar,
    ContentFooter,
    DashboardContent,
    MobileMenu,
  },
  methods: {
    toggleSidebar() {
      if (this.$sidebar.showSidebar) {
        this.$sidebar.displaySidebar(false);
      }
    },
  },
};
</script>
