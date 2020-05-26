<template>
  <header>
    <h1>{{ newTitle }}</h1>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    title: String
  },
  data() {
    return {
      name: "Tony"
    };
  },
  computed: {
    newTitle: function() {
      return this.title
        .split("")
        .reverse()
        .join("");
    }
  }
};
</script>

<style scoped>
header {
  background-color: #111;
  padding: 20px;
  color: white;
}

h1 {
  margin: 0;
}
</style>