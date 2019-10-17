<template>
  <aside class="sidebar left-sidebar">
    <ul class="sidebar__nav">
        <sidebarItem v-for="(item, index) in menu" :key="index" :item="item"></sidebarItem>
    </ul>
  </aside>
</template>

<script>
import sidebarItem from './sidebarItem'
export default {
    props: [
      'menu'
    ],
    components: {
        sidebarItem
    }
}
</script>

<style lang="scss">
  @import "../../assets/scss/variables";
  @import "./sidebar";
</style>