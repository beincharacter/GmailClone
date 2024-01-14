<template>
  <div id="EmailView" class="bg-gray-50 h-screen">
    <div class="flex items-center p-2">
      <div class="logo-section flex justify-start items-center px-3.5">
        <IconComponent
          iconString="menu"
          iconColor="#636363"
          :iconSize="19"
          hoverColor="hover:bg-gray-200"
          text="Main menu"
          class="-ml-2 mr-2"
        />
        <img src="../../assets/img/GmailLogo.png" alt="logo" width="107" />
      </div>
      <div class="flex w-650 mr-auto justify-between" style="width: 650px">
        <div class="w-full bg-gray-200 flex items-center p-1 px-2 rounded-lg">
          <IconComponent
            iconString="magnify"
            iconColor="#636363"
            :iconSize="19"
            hoverColor="hover:bg-gray-200"
            text="Search"
            class="-ml-2 mr-2"
          />
          <input
            type="text"
            placeholder="Seach email"
            class="w-full h-10 bg-gray-200 border-transparent border-none focus:ring-0 outline-none placeholder-gray-900"
          />
          <IconComponent
            iconString="tune"
            iconColor="#636363"
            :iconSize="19"
            hoverColor="hover:bg-gray-200"
            text="show filters"
            class="-ml-2 mr-2"
          />
        </div>
      </div>
      <div class="flex justify-between items-center w-32 ml-6">
        <IconComponent
          iconString="cog"
          iconColor="#636363"
          :iconSize="19"
          hoverColor="hover:bg-gray-200"
          text="Settings"
        />
        <IconComponent
          iconString="apps"
          iconColor="#636363"
          :iconSize="19"
          hoverColor="hover:bg-gray-200"
          text="Google apps"
        />
        <UserComponent />
      </div>
    </div>

    <!-- left right panels -->
    <div class="flex w-full">
      <div id="SideMenu" class="sidemenu">
        <div
          class="flex items-center justify-center bg-sky-200 w-36 h-8 mt-2 rounded-2xl ml-2 p-7 cursor-pointer"
        >
          <PencilOutlineIcon :size="25" class="mr-4" />
          <span class="text-sm">Compose</span>
        </div>
        <div class="my-5"></div>

        <div
          class="side-menu-item flex justify-between px-6 py-1.5 bg-blue-100 rounded-full cursor-pointer"
        >
          <div class="flex items-center">
            <InboxIcon :size="15" />
            <div class="text-sm pl-4 font-semibold">Inbox</div>
          </div>
          <div class="text=xs font-semibold">26</div>
        </div>

        <div class="side-menu-item flex justify-between px-6 py-1.5 cursor-pointer">
          <div class="flex items-center">
            <StarredIcon :size="15" />
            <div class="text-sm pl-4">Starred</div>
          </div>
        </div>

        <div class="side-menu-item flex justify-between px-6 py-1.5 cursor-pointer">
          <div class="flex items-center">
            <SnoozIcon :size="15" />
            <div class="text-sm pl-4">Snoozed</div>
          </div>
        </div>

        <div class="side-menu-item flex justify-between px-6 py-1.5 cursor-pointer">
          <div class="flex items-center">
            <SentIcon :size="15" />
            <div class="text-sm pl-4">Sent</div>
          </div>
        </div>

        <div class="side-menu-item flex justify-between px-6 py-1.5 cursor-pointer">
          <div class="flex items-center">
            <DraftIcon :size="15" />
            <div class="text-sm pl-4">Draft</div>
          </div>
        </div>
      </div>

      <!-- this is where out page chgange -->
      <router-view />
      <!-- this is where out page chgange -->

      
    </div>
  </div>
</template>

<script lang="ts" setup>
import IconComponent from "@/components/IconComponent.vue";
import UserComponent from "@/components/UserComponent.vue";
import PencilOutlineIcon from "vue-material-design-icons/PencilOutline.vue";
import InboxIcon from "vue-material-design-icons/InboxOutline.vue";
import StarredIcon from "vue-material-design-icons/StarOutline.vue";
import SnoozIcon from 'vue-material-design-icons/ClockOutline.vue';
import SentIcon from 'vue-material-design-icons/SendOutline.vue';
import DraftIcon from 'vue-material-design-icons/FileOutline.vue'
</script>

<style lang="scss">
#EmailView {
  .logo-section {
    min-width: 250px;
  }

  .side-menu {
    width: 300px;
  }

  .side-menu-item {
    width: 250px;
  }
}
</style>
