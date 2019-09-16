<template>
  <div class="hello" id="app">
    <h1>{{ msg }}</h1>

    <h3>THE LANGUAGES OF APPRECIATION PROFILE</h3>
    <!-- <p>Circle the letter from each pair that you feel is most important to you. Sometimes both will be important to you (or sometimes neither will be especially significant to you). Please choose the one that is the most important to you of the pair presented. Do not spend a lot of time on each question; go with your first response.</p> -->

    <ul id="example-1">
      <li v-for="item in items" :key="item.id">{{ item.message }}</li>
    </ul>

    <span>Selected Ids: {{ userIds }}</span>
  </div>
</template>

<script>
console.log("ran");
var example1 = new Vue({
  el: "#example-1",
  data: {
    items: [{ message: "Foo" }, { message: "Bar" }]
  }
});
</script>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
