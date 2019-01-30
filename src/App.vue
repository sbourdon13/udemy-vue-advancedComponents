<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <!-- <button @click="selectedComponent = 'appQuote'">Quote</button>
        <button @click="selectedComponent = 'appAuthor'">Author</button>
        <button @click="selectedComponent = 'appNew'">New</button>
        <hr>
        <p>{{ selectedComponent }}</p>
        <keep-alive>
          <component :is="selectedComponent">
            <p>Default content</p>
          </component>
        </keep-alive>-->
        <br>
        <button class="btn btn-primary" @click="selectedTemplate = 'appBlue'">Load Blue Template</button>
        <button
          class="btn btn-success"
          @click="selectedTemplate = 'appGreen'"
          style="margin: 0 20px"
        >Load Green Template</button>
        <button class="btn btn-danger" @click="selectedTemplate = 'appRed'">Load Red Template</button>
        <hr>
        <keep-alive>
          <component :is="selectedTemplate">
            <h3>Your amazing quote:</h3>
            <em>In ancient times cats were worshipped as gods; they have not forgotten this.</em>
            <p>
              By
              <strong>Terry Pratchett</strong>
            </p>
          </component>
        </keep-alive>
      </div>
    </div>
  </div>
</template>

<script>
// import Quote from "./components/Quote";
// import Author from "./components/Author";
// import New from "./components/New";
import Blue from "./components/Blue.vue";
import Green from "./components/Green.vue";
import Red from "./components/Red.vue";

export default {
  data() {
    return {
      selectedComponent: "appQuote",
      selectedTemplate: "appBlue"
    };
  },
  components: {
    // appQuote: Quote,
    // appAuthor: Author,
    // appNew: New,
    appBlue: Blue,
    appGreen: Green,
    appRed: Red
  }
};
</script>

<style scoped>
h2 {
  color: blue;
}
</style>
