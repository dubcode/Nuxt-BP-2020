<template>
  <div id="header-state" class="block" :class="{'active': menuClose, 'inactive': !menuClose}">
    <header class="fixed z-50 flex bg-black w-full mx-auto my-0 px-10 py-3" :class="{'active': menuClose, 'inactive': !menuClose}">
      <div class="flex-grow text-gray-700 w-0">
        <Icons />
      </div>
      <div class="flex-none w-8">
        <Logo />
      </div>
      <div class="flex flex-grow justify-end items-center w-0">
        <Nav />
        <Hamburger :menu-close="menuClose" @toggle="menuClose = !menuClose" />
      </div>
    </header>
    <Menu />
  </div>
</template>

<script>
import Icons from '~/components/Icons.vue'
import Logo from '~/components/Logo.vue'
import Nav from '~/components/Nav.vue'
import Hamburger from '~/components/Hamburger.vue'
import Menu from '~/components/Menu.vue'
export default {
  components: {
    Icons,
    Logo,
    Nav,
    Hamburger,
    Menu
  },
  props: {
    menuClose: Boolean
  }
}
</script>
