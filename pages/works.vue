<template>
  <div>
    <NavBar />
    <Works />
    <Footer />
  </div>
</template>

<script>
import Footer from '../components/Footer.vue';
import NavBar from "../components/NavBar.vue";
import Works from "../components/Works.vue";

export default {
  name: "WorksPage",
  components: {
    NavBar,
    Works,
    Footer,
  },
  head() {
    return {
      title: "Works",
    };
  },
};
</script>
