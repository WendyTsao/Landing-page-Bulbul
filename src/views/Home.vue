<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-12 col-lg-3">
        <Menu></Menu>
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
import Intro from '../components/Into.vue';
import Menu from '../components/Menu.vue';

export default {
  components: {
    Intro, Menu
  },
};
</script>
