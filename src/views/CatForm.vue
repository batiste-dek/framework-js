
<template>
<div>
  <Header></Header>
    <div class="form">
      

          <section class="container">
            <h2>Cat card form</h2>
            <hr />
            <h3 id="formError" class="text-center text-danger d-none"></h3>
            <form id="cardForm" novalidate>
              <div class="form-group row">
                <label for="cardTitle" class="col-sm-2 col-form-label">Card title</label>
                <input type="text" required class="form-control col-sm-10" id="cardTitle" placeholder="Card title">
                <div class="invalid-feedback offset-md-2 col-sm-10">
                  That field is required. Please provide a value.
                </div>
              </div>
              <div class="form-group row">
                <label for="cardImage" class="col-sm-2 col-form-label">Card image URL</label>
                <input type="url" required class="form-control col-sm-10" id="cardImage" placeholder="Card image URL">
                <div class="invalid-feedback offset-md-2 col-sm-10">
                  That field is required and attempt an URL as value. Please provide a value that respect URL format.
                </div>
              </div>
              <div class="form-group row">
                <label for="cardDescription" class="col-sm-2 col-form-label">Card description</label>
                <textarea class="form-control col-sm-10" id="cardDescription"></textarea>
              </div>
              <input type="hidden" id="cardId">
              <button class="btn btn-danger">Delete</button>
              <button type="submit" class="btn btn-primary">Save</button>
            </form>
          </section>

        <b-form>
          <b-form-group id="input-group-2" label="Card Title:" label-for="input-2">
            <b-form-input
              id="input-2"
              v-model="form.title"
              required
              placeholder="Enter title"
              :state="isTitleValid"
              :invalid-feedback="invalidFeedback"
            ></b-form-input>
          </b-form-group>
        </b-form>

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
      // validation() {
      //   return this.form.title.length > 0
      // }

      isTitleValid() {
        console.log('COUCOU',this.form.title.length )
        if(this.form.title.length > 0) {
          return true;
        }
        return false;
      },

      invalidFeedback() {
        if (this.form.title.length > 0) {
          return 'Enter at least 1 characters.'
        }
        return 'Please enter something.'
      }
  }
};
</script>
