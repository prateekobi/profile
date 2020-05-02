<template>
  <div class="home">
    <home-view />
    <enquire-view />
  </div>
</template>

<script>
// @ is an alias to /src
import HomeView from "@/components/Home.vue";
import EnquireView from "@/components/Enquire.vue";

export default {
  name: "Home",
  components: {
    HomeView,
    EnquireView
  }
};
</script>
