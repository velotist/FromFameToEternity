<template>
  <div id="app">
    <div class="content">
      <header class="header">
        <Header />
      </header>
      <div>
        <Main />
      </div>
      <footer class="footer">
        <Footer />
      </footer>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
};
</script>

<style>
html,
body {
  /* IE 10-11 didn't like using min-height */
  height: 100%;
}
body {
  text-align: center;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.content {
  flex: 1 0 auto; /* Prevent Chrome, Opera, and Safari from letting these items shrink to smaller than their content's default minimum size. */
  padding: 20px;
}
.footer,
.header {
  flex-shrink: 0; /* Prevent Chrome, Opera, and Safari from letting these items shrink to smaller than their content's default minimum size. */
  padding: 25px;
}
* {
  box-sizing: border-box;
}
body {
  margin: 0;
  font: 16px Sans-Serif;
}
h1 {
  margin: 0 0 20px 0;
}
p {
  margin: 0 0 20px 0;
  text-align: left;
}
header,
footer {
  text-align: center;
  background: #007bff;
  color: #fff;
}
</style>
