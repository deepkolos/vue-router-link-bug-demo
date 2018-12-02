<template>
  <div class="hello">
    <p>
      router-view is wrapped with keepAlive<br>
      now this a tag' classList is "f-link default-link" <br>
      go to test page and come back<br>
      then this a tag' classList is ""
    </p>

    <f-link class="default-link" to="/test">
      go to test page
    </f-link>
  </div>
</template>

<script>
import FLink from "./f-link";

export default {
  name: "HelloWorld",
  components: { FLink },
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a.default-link {
  color: #42b983;
}
</style>
