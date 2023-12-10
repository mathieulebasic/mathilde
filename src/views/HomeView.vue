<template>
  <div class="home">
    <carreProjet />
  </div>
</template>

<script>
import carreProjet from "@/components/carreProjet.vue";

export default {
  name: "HomeView",
  components: { carreProjet },
};
</script>

<style>
.home {
  width: 100%;
  height: 100%;
  background-color: #f5f5f5;
}
</style>
