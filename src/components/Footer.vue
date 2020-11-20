<template>
  <footer class="bg-light">
    <div class="container text-center">
      <i class="far fa-copyright mr-1"></i
      ><label><span id="currentYear">2017</span> - Lille 1</label>
      <span class="small font-italic infos"
        >No cat has been hurt during the development of this app.</span
      >
    </div>
  </footer>
</template>

<script lang="ts">
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";
import Vue from "vue";

export default Vue.extend({
  name: "Footer",
});
</script>

<style>
footer {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 60px;
  line-height: 60px;
}
</style>