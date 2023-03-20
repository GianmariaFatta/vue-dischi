<script>
const baseProjectsUrl = "http://127.0.0.1:8000/api";
import axios from "axios";
export default {
  name: "VideogameDetailPage",
  data() {
    return {
      videogame: null,
    };
  },
  methods: {
    fetchVideogame() {
      const endpoint = baseProjectsUrl + "/videogame/" + this.$route.params.id;
      axios
        .get(endpoint)
        .then((res) => {
          this.videogame = res.data;
        })
        .catch(() => {
          this.$router.push({ name: "not-found" });
        })
        .then(() => {});
    },
  },
  created() {
    this.fetchVideogame();
  },
};
</script>

<template>
  <div class="container">
    <h1 class="text-center">{{ videogame.title }}</h1>
  </div>
</template>

<style></style>
