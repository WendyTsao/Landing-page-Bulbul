<template>
  <div class="navbar">
    <div class="menubar">
      <a class="menubar-open">
        <i class="fas fa-bars"></i>
      </a>
      <h3>白頭翁不吃小米</h3>
      <div class="logo"></div>
    </div>
    <div class="menu-item">
      <ul v-for="menu in menuItems" class="item" :key="menu.item">
        <li>
          <a href="#">{{ menu.item }}</a>
        </li>
      </ul>
    </div>
    <div class="copyright">&copy;</div>
  </div>
</template>

<script>
export default {
  setup() {
    const menuItems = [
      { item: "白頭翁的特性" },
      { item: "白頭翁的故事" },
      { item: "白頭翁的美照" },
      { item: "白頭翁的危機" },
    ];

    return { menuItems };
  },
};
</script>

<style>
</style>