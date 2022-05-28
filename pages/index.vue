<template>
  <div>
    <NavBar />
    <Home />
    <Footer />
  </div>
</template>

<script>
import NavBar from "../components/NavBar.vue";
import Home from "../components/Home.vue";
import Footer from '../components/Footer.vue';

export default {
  name: "IndexPage",
  components: {
    NavBar,
    Home,
    Footer,
  },
};
</script>
