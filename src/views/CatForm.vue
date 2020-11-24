
<template>
<div>
  <Header></Header>
    <div class="form">
            <h2>Cat card form</h2>
            <hr />
      

                  <b-container fluid>
  <b-row class="my-1">
    <b-col sm="3">
      <label for="input-1">Card title</label>
    </b-col>
    <b-col sm="9">
      <b-form-input
              id="input-1"
              v-model="form.title"
              required
              placeholder="Card title"
              :state="this.form.title.length > 0"

            ></b-form-input>
    </b-col>
  </b-row>

  <b-row class="my-1">
    <b-col sm="3">
      <label for="input-2">Card image URL</label>
    </b-col>
    <b-col sm="9">

      <b-form-input
              id="input-2"
              v-model="form.url"
              required
              placeholder="Card image URL"
              :state="isUrlValid"

            ></b-form-input>

    </b-col>
  </b-row>

  <b-row class="my-1">
    <b-col sm="3">
      <label for="input-3">Card description</label>
    </b-col>
    <b-col sm="9">

      <b-form-textarea
              id="input-3"
              v-model="form.description"
            ></b-form-textarea>

    </b-col>
  </b-row>
</b-container>

    <button type="submit" class="btn btn-primary">Save</button>


    </div>
  <Footer></Footer>
</div>
</template>


<script lang="ts">
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";
import Vue from "vue";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Form",
  components: {
    Header,
    Footer
  },
  data() {
    return {
      form : {
        title : '',
        url : '',
        description : ''
      }
    }
  },
  computed: {
    isTitleValid() {
        if((this as any).form.title.length > 0) {
          return true;
        }
        return false;
      },
    isUrlValid() {
      const url = (this as any).form.title;
      if(url.length > 0 && url.substring(0, 7) === "http://") {
          return true;
        }
        return false;
    }
  }
};
</script>
