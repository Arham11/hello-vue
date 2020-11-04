<template>
  <h1>{{ myName }}</h1>
  <p></p>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      myName: "Arham Chowdhury"
    };
  },
  beforeCreate() {
    console.log(
      `"beforeCreated() is exected after App is created in main.js" ${this.myName}`
    );
  },
  created() {
    console.log(
      `"Created() is exected after logic i.e data() of component is loaded" ${this.myName}`
    );
  },
  beforeMount() {
    console.log(
      `"beforeMount is exected when component view is getting loaded"`
    );
  },
  mounted() {
    console.log(
      `"mounted is exceuted when component view and logic is loaded" ${this.myName}`
    );
  }
};
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
