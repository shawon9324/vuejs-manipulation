<template>
  <div>
    <nav>
      <ul>
        <li><a href="">HOME</a></li>
        <li><a href="">POST</a></li>
        <li><a href="">ABOUT</a></li>
        <li><a href="">CONTACT</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {};
  },
};
</script>
 
<style scoped>
nav {
  text-align: center;
}
nav ul {
  padding: 0;
}
nav li {
  display: inline-block;
  list-style: none;
  margin: 0;
  padding: 8px;
}
</style>
