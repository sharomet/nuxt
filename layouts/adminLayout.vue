<template>
  <div class="wrapper">
    <navbar/>
    <div class="wrapper-content">
      <sidebar :menu="sidebarMenu" />
      <div class="content">
        <nuxt/>
      </div>
    </div>
  </div>
</template>

<script>
import navbar from '@/components/adminNavbar/navbar'
import sidebar from '@/components/adminSidebar/sidebar'

export default {
  data() {
    return {
        sidebarMenu: [
            {
                href: '/admin/dashboard',
                title: 'Dashboard',
                icon: 'fas fa-tachometer-alt',
            },
            {
                href: '/admin/components',
                title: 'Components',
                icon: 'fas fa-cubes'
            },
            {
                href: '/admin/users',
                title: 'Users',
                icon: 'fas fa-users',
                child: [
                    {
                        href: '/admin/sublink',
                        title: 'Sub Link',
                    },
                    {
                        href: '/admin/sublink',
                        title: 'Sub Link 2',
                    },
                    {
                        href: '/admin/sublink',
                        title: 'Sub Link 3',
                    }
                ]
            },
        ],
    }
  },
  components: {
    navbar,
    sidebar
  }
  
}
</script>