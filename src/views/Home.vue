<template>
  <div>
    <Header></Header>
    <section class="container">
      <h2>Cat card list</h2>
      <hr />
      <div class="card-group"></div>
      <router-link class="btn btn-danger circle add" to="/cat-form">
        <b-icon icon="plus"></b-icon>
      </router-link>
      <Footer></Footer>
    </section>
  </div>
</template>

<script lang="ts">
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";
import Vue from "vue";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";

export default Vue.extend({
  name: "Home",
  components: {
    Header,
    Footer
  }
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
</style>
