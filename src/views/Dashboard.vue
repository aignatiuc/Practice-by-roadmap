<template>
  <div class="relative flex flex-col h-full min-h-screen">
    <div class="w-full bg-orange-100 top-bar" />

    <dashboard-header />

    <v-main class="z-0 flex-grow">
      <router-view />
    </v-main>

    <dashboard-footer />
  </div>
</template>

<script>
import DashboardHeader from "@/components/dashboard/DashboardHeader";
import DashboardFooter from "@/components/dashboard/DashboardFooter";

export default {
  components: {
    DashboardHeader,
    DashboardFooter,
  },
};
</script>

<style scoped>
.top-bar {
  height: 3px;
}
</style>
