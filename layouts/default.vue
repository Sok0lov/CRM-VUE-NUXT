<template>
  <section class="side-bar grid">
    <LayoutSideBar />
      <div>
        <slot/>
      </div>
  </section>
</template>

<script lang='ts' setup>

import SideBar from "~/components/layout/SideBar.vue";
</script>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: 1fr 6fr;
}

.side-bar {
  min-height: 100vh;
}

</style>