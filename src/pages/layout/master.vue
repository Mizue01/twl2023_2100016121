<template>
  <div id="app" v-bind:style="{ backgroundImage: 'url(' + require('@/assets/images/Sunsett.png') + ')', backgroundSize: 'cover',backgroundPosition: 'center' }">
  <div class="w-full h-full flex">
    <sidebar :dataOpenSideBar="openSidebar" />
    <div class="w-full h-full">
      <headerTop :dataOpenSideBar="openSidebar" :clickHambuger="toggleSidebar" />
      <div class="w-full h-[calc(100vh-50px)z]">
        <router-view></router-view>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import headerTop from './../../components/header.vue'
import sidebar from './../../components/sidebar.vue'

export default {
  components: { headerTop, sidebar },
  data() {
    return {
      openSidebar: true
    }
  },
  methods: {
    toggleSidebar() {
      this.openSidebar = !this.openSidebar
    }
  }

}
</script>

<style>

</style>