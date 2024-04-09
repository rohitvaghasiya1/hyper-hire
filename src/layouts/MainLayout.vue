<template>
  <q-layout view="hHh lpR fFf">
    <q-header :reveal="true" class="bg-transparent">
      <q-toolbar class="container">
        <!-- Logo, visible on both mobile and desktop -->
        <img src="/assets/logo.png" class="q-mr-md" />
        <!-- Spacer to push elements to the sides -->
        <q-space />

        <!-- Navigation items visible only on desktop -->
        <template v-if="!isMobile">
          <div class="q-gutter-md" style="display: flex; align-items: center">
            <!-- Services Dropdown -->
            <q-btn
              dropdown
              flat
              label="채용"
              class="text-white custom-dropdown"
              color="primary"
              :no-caps="true"
              :no-wrap="true"
              icon-right="expand_more"
            >
              <q-menu>
                <q-list style="min-width: 100px">
                  <!-- Adjust min-width as needed -->
                  <q-item clickable v-ripple to="/service1">
                    <q-item-section>채용</q-item-section>
                  </q-item>
                  <q-item clickable v-ripple to="/service1">
                    <q-item-section>해외 개발자 원격 채용</q-item-section>
                  </q-item>
                  <q-item clickable v-ripple to="/service1">
                    <q-item-section
                      >외국인 원격 채용 (비개발 직군)</q-item-section
                    >
                  </q-item>
                  <q-item class="seperator" clickable v-ripple to="/service1">
                    <q-item-section>한국어 가능 외국인 채용</q-item-section>
                  </q-item>
                  <!-- Additional service items -->
                </q-list>
              </q-menu>
            </q-btn>

            <!-- About Us Link -->
            <q-btn
              flat
              label="해외 개발자 활용 서비스"
              to="/about"
              class="text-white"
            />
          </div>

          <!-- Spacer to align Contact Us button to the right -->
          <q-space />

          <!-- Contact Us Button -->
          <q-btn
            color="white"
            text-color="black"
            label="문의하기"
            to="/contact"
            class="text-white"
          />
        </template>

        <!-- Hamburger menu icon, only shown in mobile view -->
        <q-btn
          icon="menu"
          v-if="isMobile"
          class="q-ml-auto"
          @click="toggleDrawer"
          color="white"
          flat
        />
      </q-toolbar>
    </q-header>

    <!-- Drawer for Mobile Navigation, includes all items -->
    <q-drawer v-model="drawer" side="right" overlay behavior="mobile">
      <q-list>
        <q-btn
          dropdown
          flat
          label="채용"
          class="custom-dropdown dark"
          color="grey-9"
          :no-caps="true"
          :no-wrap="true"
          icon-right="expand_more"
        >
          <q-menu>
            <q-list style="min-width: 100px">
              <!-- Adjust min-width as needed -->
              <q-item clickable v-ripple to="/service1">
                <q-item-section>채용</q-item-section>
              </q-item>
              <q-item clickable v-ripple to="/service1">
                <q-item-section>해외 개발자 원격 채용</q-item-section>
              </q-item>
              <q-item clickable v-ripple to="/service1">
                <q-item-section>외국인 원격 채용 (비개발 직군)</q-item-section>
              </q-item>
              <q-item class="seperator" clickable v-ripple to="/service1">
                <q-item-section>한국어 가능 외국인 채용</q-item-section>
              </q-item>
              <!-- Additional service items -->
            </q-list>
          </q-menu>
        </q-btn>
        <q-item clickable v-ripple to="/about">
          <q-item-section>해외 개발자 활용 서비스</q-item-section>
        </q-item>
        <!-- Additional drawer items -->
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
    <FooterView />
  </q-layout>
</template>

<script>
import { ref, computed } from "vue";
import { useQuasar } from "quasar";
import FooterView from "../components/global/FooterView.vue";
export default {
  components: {
    FooterView,
  },
  setup() {
    const $q = useQuasar();
    const drawer = ref(false);

    const isMobile = computed(() => $q.screen.xs);

    function toggleDrawer() {
      drawer.value = !drawer.value;
    }

    return {
      drawer,
      isMobile,
      toggleDrawer,
    };
  },
};
</script>

<style lang="scss">
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 15px;
}

.bg-transparent {
  background: transparent;
}

.seperator {
  border-top: 1px solid #f2f4f7;
}

.custom-dropdown {
  background-color: transparent !important;
  border: none !important;
  .q-btn__wrapper {
    color: white !important;
  }
  .q-icon {
    color: white !important;
  }
  &.dark {
    .q-icon {
      color: rgb(8, 6, 6) !important;
    }
  }
}
</style>
