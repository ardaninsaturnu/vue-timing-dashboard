<template>
  <div class="dashboard">
    <div class="sidebar">
      <div class="personal-wrapper">
        <div class="img-wrapper" :style="{ backgroundImage: `url(${require('@/assets/image-jeremy.png')})` }"></div>
        <div class="text-wrapper">
          <p>Report for</p>
          <h1>Jeremy Robson</h1>
        </div>
      </div>
      <div class="route-wrapper">
        <router-link to="/">Daily</router-link>
        <router-link to="/weekly-view">Weekly</router-link>
        <router-link to="/monthly-view">Monthly</router-link>
      </div>
    </div>
    <!-- here is list rendering -->
    <div class="card-grid-wrapper">
      <slot/>
    </div>
  </div>
</template>

<script>
export default {
  name: "DashboardComponent",
  props: {
    profile: String
  }
}
</script>

<style lang="scss" scoped>
  @import "src/styles/dashboard.scss";
</style>