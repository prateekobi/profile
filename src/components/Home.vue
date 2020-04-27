<template>
  <div class="home container-fluid">
    <div class="nav float-right">
      <p class="mr-5">About me</p>
      <p class="mr-2">Enquire</p>
    </div>
    <div class="container text-center">
      <img src="../assets/name.jpeg" alt />
      <!-- <img src="../assets/role.jpeg" alt /> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "Home"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.home {
  img {
    // display: block;
    height: 260px;
  }
  padding: 30px;
  background-color: #e0ebe8;
  height: 100vh;
  font-family: "Comic Sans MS";
  color: #6eb4c7;
  .nav {
    p {
      font-size: 20px;
    }
  }
}
</style>
