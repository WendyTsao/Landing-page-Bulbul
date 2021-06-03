<template>
  <div class="navbar">
    <div class="menubar">
      <a class="menubar-open" @click="openMenu">
        <i class="fas fa-bars"></i>
      </a>
      <h3>白頭翁不吃小米</h3>
      <div class="logo"></div>
    </div>
    <div class="menu-item">
      <ul class="item" >
        <li v-for="menu in menuItems" :class="{'hidden-menu':menubarStatus}" :key="menu.item">
          <a href="#">{{ menu.item }}</a>
        </li>
      </ul>
      <div :class="['copyright',{'hidden-copyright':menubarStatus}]">&copy;</div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const menuItems = [
      { item: "白頭翁的特性" },
      { item: "白頭翁的故事" },
      { item: "白頭翁的美照" },
      { item: "白頭翁的危機" },
    ];

    const menubarStatus = ref(false);
    const openMenu = ()=> {
      menubarStatus.value = !menubarStatus.value
    };

    return { menuItems, menubarStatus, openMenu };
  },
};
</script>

<style scoped>
  .show-menu{ 
      height: 24px;
      padding: 10px 0;
  }
  .hidden-menu{ 
      height: 0;
      padding: 0;
      margin: 0;
  }
  .hidden-copyright{
    display: none;
  }
</style>