<template>
  <nav class="nav-main">
    <h2>{{ title }}</h2>
    <ul>
      <li>
        <a href>Home</a>
      </li>
      <li>
        <a href>Contact</a>
      </li>
      <li>
        <a href>About</a>
      </li>
    </ul>
  </nav>
</template>
<script>
export default {
  name: "Navbar",
  data() {
    return {
      title: "Menu"
    };
  }
};
</script>
<style>
nav.nav-main {
  text-align: center;
}
nav.nav-main {
  padding: 0px;
}
nav.nav-main ul li {
  display: inline-block;
  list-style-type: none;
  padding-right: 10px;
}
</style>