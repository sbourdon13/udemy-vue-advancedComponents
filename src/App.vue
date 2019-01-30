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
        <button class="btn btn-primary">Load Blue Template</button>
        <button class="btn btn-success" style="margin: 0 20px">Load Green Template</button>
        <button class="btn btn-danger">Load Red Template</button>
        <hr>
        <app-blue></app-blue>
        <app-green></app-green>
        <app-red></app-red>
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
      selectedComponent: "appQuote"
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
