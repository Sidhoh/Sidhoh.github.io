<template>
  <div>
    <NavBar />
    <Gallery />
    <Footer />
  </div>
</template>

<script>
import NavBar from "../components/NavBar.vue";
import Gallery from "../components/Gallery.vue";
import Footer from '../components/Footer.vue';

export default {
  name: "GalleryPage",
  components: {
    NavBar,
    Gallery,
    Footer,
  },
  head() {
    return {
      title: "Gallery",
    };
  },
};
</script>
