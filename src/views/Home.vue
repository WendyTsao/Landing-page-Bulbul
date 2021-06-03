<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-12 col-lg-3">
        <div class="navbar">
          <div class="menubar">
            <a class="menubar-open">
              <i class="fas fa-bars"></i>
            </a>
            <h3>白頭翁不吃小米</h3>
            <div class="logo"></div>
          </div>
          <div class="menu-item">
            <ul class="item">
              <li><a href="#">白頭翁的特性</a></li>
              <li><a href="#">白頭翁的故事</a></li>
              <li><a href="#">白頭翁的美照</a></li>
              <li><a href="#">白頭翁的危機</a></li>
              <li>&copy;</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="col-12 col-lg-9">
        <div class="col-12">
          <div class="banner">
            <div class="container">
              <div class="txt">
                <h1>白頭翁(Chinese bulbul)</h1>
                <p>
                  又名白頭鵯。以果實、昆蟲為主食，無法消化小米、穀類。平均壽命約
                  8~10 年。
                </p>
              </div>
            </div>
          </div>
        </div>
        <Intro></Intro>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Intro from '../components/intro.vue';

export default {
  components: {
    Intro,
  },
};
</script>
