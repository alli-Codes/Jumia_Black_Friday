<template>
  <div id="header"
    class="bg-white h-20 w-full flex items-stretch justify-center sticky top-0 z-[1000] shadow-md relative">
    <div class="w-9/12 flex items-center justify-evenly">
      <img src="../../assets/logo.png" class="w-32">

      <div id="search__container" class="h-10 flex items-center justify-center flex-auto  w-64 px-20 gap-2 ">
        <div id="search__inner"
          class="bg-white flex flex-1 items-center px-3 self-stretch border-solid border border-gray-300 rounded">
          <Icon icon="eva:search-outline" width="24" color="gray" />
          <input type="text" class="p-3 self-stretch flex-1 outline-none"
            placeholder="Search products, brands and categories">
        </div>
        <button
          class="bg-[#f68b1e] hover:bg-orange-500 self-stretch p-3 w-24 font-semibold text-sm text-white rounded shadow-md">SEARCH</button>
      </div>

      <div id="user__section" class="w-80 flex justify-evenly font-semibold relative">
        <div class="open:bg-white relative">
          <a @click="dropDown" id="dropdownDefault" data-dropdown-toggle="dropdownId"
            class="flex items-center cursor-pointer hover:text-orange-400 gap-1">
            <Icon icon="la:user-check" width="25" />
            <p>Hi, Evans</p>
            <Icon icon="charm:chevron-down" width="15" />
          </a>

          <AccountModal v-show="showModal" />
        </div>

        <a id="user__support" class="flex items-center cursor-pointer hover:text-orange-400 gap-1">
          <Icon icon="charm:help" width="25" />
          <p>Help</p>
          <Icon icon="charm:chevron-down" width="15" />
        </a>

        <!-- AccountModal v-show="showModal" /> -->

        <a id="user__cart" class="flex gap-1 cursor-pointer hover:text-orange-400 relative">
          <Icon icon="ic:outline-shopping-cart" width="25" />
          <p
            class="h-4 w-4 flex items-center justify-center text-[10px] bg-orange-400 text-white rounded-full border-solid border-2 border-white absolute left-[12px]">
            1</p>
          <p>Cart</p>
        </a>
      </div>
    </div>

  </div>
</template>

<script>
import { Icon } from '@iconify/vue';
import AccountModal from './AccountModal.vue';
export default {
  name: "HeaderTag",
  components: {
    Icon,
    AccountModal
},
  data() {
    return {
      showModal: false
  }
},
  methods: {
    dropDown() {
      !this.showModal ? this.showModal = true : this.showModal = false
    }
}
};
</script>
