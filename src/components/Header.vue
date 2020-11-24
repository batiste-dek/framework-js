<template>
  <header class="bg-primary">
    {{getUrl}}
    <a v-if="!isRoot" v-bind:style="styleObject" href="/" class="btn btn-primary back-btn"><i class="fas fa-caret-left mr-2"></i>Back</a>
    <h1 class="text-white text-center p-3">Cat card app</h1>
  </header>
</template>

<script lang="ts">
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";
import Vue from "vue";

export default {
  name: "Header",

  data() {
    return {
      styleObject: {
        position: 'absolute',
        top: '20px',
        left: '20px'
      },

      isRoot: window.location.toString() === 'http://localhost:8080/#/' ||
              window.location.toString() === 'http://localhost:8080/',
    }
  },


};
</script>
