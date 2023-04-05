<template>
  <div class="h-screen   bg-gray-800" id="side-bar" :class="dataOpenSideBar == true ? 'side-bar-visible' : 'side-bar-close'">
    <div class="bg-gray-800 h-[50px] flex justify-center items-center ">
      <div class="text-xl font-bold text-center flex items-center justify-center text-white h-full" v-show="dataOpenSideBar">Shopping Web</div>
      <img src="../assets/images/redpandass.jpg" v-show="!dataOpenSideBar" class="p-1 w-8 h-8 rounded-full ring-2 ring-gray-100 dark:ring-gray-500 " alt="Avatar" />
    </div>
    <div class="flex flex-col justify-between h-[calc(100vh-3rem)] bg-gray-900">
      <div class="menu-man text-left px-2 whitespace-nowrap ">
        <div class="profile flex justify-center items-center text-center p-5 ">
          <div class="text-center  text-white" v-show="dataOpenSideBar">
            <img src="../assets/images/redpandass.jpg" class="p-1 w-24 h-24 rounded-full ring-2 ring-gray-300 dark:ring-gray-500 mb-4" alt="Avatar" />
            <h5 class="text-xl font-medium leading-tight mb-2"> Red Panda</h5>
            <p class="text-gray-500">Profile </p>
          </div>
        </div>
        <div class="   py-3 rounded-sm cursor-pointer text-gray-300 hover:text-white">
          <router-link to="/" class="px-2 flex space-x-2"><span class="pi pi-eject" v-tooltip.right="'Dashboard'"></span> <span v-show="dataOpenSideBar">Home</span></router-link>
        </div>
        <div class="   py-3 rounded-md cursor-pointer  text-gray-300 hover:text-white">
          <router-link to="/user" class="px-2 flex space-x-2"><span class="pi pi-map-marker " v-tooltip.right="'User'"></span> <span v-show="dataOpenSideBar">Shop Location</span></router-link>
        </div>
        <div class="   py-3 rounded-md cursor-pointer  text-gray-300 hover:text-white">
          <router-link to="/product" class="px-2 flex space-x-2"><span class="pi pi-shopping-cart " v-tooltip.right="'Product'"></span> <span v-show="dataOpenSideBar">Product</span></router-link>
        </div>
        <div class="  py-3 rounded-md cursor-pointer text-gray-300 hover:text-white">
          <div class="px-2 flex space-x-2"><span class="pi pi-cog" v-tooltip.right="'Setting'"></span> <span v-show="dataOpenSideBar">Setting</span></div>
        </div>

      </div>
      <div class="menu-man text-left px-2 justify-self-end whitespace-nowrap">
        <div class="py-3 rounded-md cursor-pointer text-gray-300 hover:text-white">
          <a href="https://osu.ppy.sh/users/27534494" target="_blank" class="px-2 flex space-x-2"><span class="pi pi-link" v-tooltip.right="'About Me'"></span> <span v-show="dataOpenSideBar">About Me</span></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    dataOpenSideBar: Boolean
  },

}
</script>

<style>
.p-tooltip-text {
  font-size: 10px !important;
}

#side-bar {
  overflow: hidden;
  transition: 300ms;
}

.side-bar-visible {
  width: 250px !important;
}

.side-bar-close {
  width: 50px !important;
}
</style>