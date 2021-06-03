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
        <li v-for="menu in menuItems" :class="{'hidden-menu':!menubarStatus}" :key="menu.item">
          <a href="#">{{ menu.item }}</a>
        </li>
      </ul>
      <div :class="['copyright',{'hidden-copyright':!menubarStatus}]">&copy;</div>
    </div>
  </div>
</template>

<script>
import { onMounted, computed, ref } from "vue";

export default {
  setup() {
    const menuItems = [
      { item: "白頭翁的特性" },
      { item: "白頭翁的故事" },
      { item: "白頭翁的美照" },
      { item: "白頭翁的危機" },
    ];

    
    const showMenu = ref(false);
    const openMenu = ()=> showMenu.value = !showMenu.value;

    const screenWidth = ref(document.body.offsetWidth);
    const isDesktop = computed(()=> screenWidth.value >= 992);

    onMounted(() => {
      document.addEventListener('scroll', ()=> showMenu.value = false);
      window.addEventListener('resize', ()=>  screenWidth.value = document.body.offsetWidth);
    });
      const menubarStatus = computed(()=> showMenu.value || isDesktop.value);


    return { menuItems, showMenu, menubarStatus, openMenu};
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