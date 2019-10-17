<template>
  <li>
    <router-link class="nav-link" :to="{ path: item.href }">
      <span>{{ item.title }}</span>
      <em v-if="item.icon" :class="item.icon"></em>
    </router-link>
    <ul v-if="item.child">
      <sidebarItem 
        v-for="(subitem, index) in item.child"
        :key="index"
        :item="subitem">
      </sidebarItem>
    </ul>
  </li>
</template>

<script>
export default {
  name: 'sidebarItem',
  props: ['item']
}
</script>