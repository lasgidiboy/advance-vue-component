<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <button @click="seletedComponent = 'New'" class="btn btn-primary">New</button>
        <button @click="seletedComponent = 'Author'" class=" btn btn-danger">Author</button>
        <button @click="seletedComponent = 'Quote'" class=" btn btn-success">Quote</button>
        <p>{{seletedComponent}}</p>
        <keep-alive>
          <component :is="seletedComponent"></component>
        </keep-alive>
        
        <!-- <appQuote>
          <h2 slot="title">{{quote}}</h2>
          <p slot="content">para</p>
        </appQuote> -->
      </div>
    </div>
  </div>
</template>

<script>
import Quote from "./component/Quote.vue";
import New from "./component/New.vue";
import Author from "./component/Author.vue";
export default {
  data() {
    return {
      quote: "The Qoute",
      seletedComponent: "appQuote"
    };
  },
 
  components: {
    appQuote: Quote,
    New,
    Author
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.rec{
  width: 1000px;
  margin: auto;
  border: 2px solid green;
  text-align: center;
  padding: 15px;
  background-color: aquamarine;
}
</style>