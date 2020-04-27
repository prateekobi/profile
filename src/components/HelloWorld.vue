<template>
  <b-card no-block>
    <b-tabs>
      <b-tab title="Tab 1">Tab 1 Contents</b-tab>
      <b-tab title="Tab 2">
        Tab 2 Contents
        <b-button size="md">Boop</b-button>
      </b-tab>
      <b-tab title="Tab 3" disabled>Tab 3 Contents</b-tab>
    </b-tabs>
  </b-card>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
