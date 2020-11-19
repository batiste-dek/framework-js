<template>
  <div>
    <header class="bg-primary">
      <h1 class="text-white text-center p-3">Cat card app</h1>
    </header>
    <section class="container">
      <h2>Cat card list</h2>
      <hr />
      <div class="card-group">
      </div>
      <router-link class="btn btn-danger circle add" to="/cat-form">
        <b-icon icon="plus"></b-icon>
      </router-link>
    </section>
    <footer class="bg-light">
      <div class="container text-center">
        <i class="far fa-copyright mr-1"></i><label><span id="currentYear">2017</span> - Lille 1</label>
        <span class="small font-italic infos">No cat has been hurt during the development of this app.</span>
      </div>
    </footer>
  </div>
</template>

<script lang="ts">
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
import Vue from "vue";

export default Vue.extend({
  name: "Home",
});
</script>

<style>
.btn.circle {
  border-radius: 50%;
}
.add {
  position: fixed;
  bottom: 80px;
  right: 20px;
}
footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 60px;
  line-height: 60px;
}
</style>