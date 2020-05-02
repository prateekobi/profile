<template>
  <div class="home container-fluid">
    <div class="nav float-right">
      <p class="mr-5">About me</p>
      <p class="mr-2">Enquire</p>
    </div>
    <div class="container text-center">
      <img class="name" src="../assets/name.jpeg" />
      <img class="role" src="../assets/role.jpeg" />
      <div class="socials">
        <a target="_blank" href="https://github.com/prateekobi">
          <i class="fab fa-github-alt"></i>
        </a>
        <a target="_blank" href="https://linkedin.com/in/prateekobi">
          <i class="fab fa-linkedin-in"></i>
        </a>
      </div>
      <img class="harbour" src="../assets/harbour.png" alt />
      <div class="chevron jump">
        <i class="fas fa-chevron-down"></i>
      </div>
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

.container {
  margin-top: 100px;
  img {
    display: block;
    margin: 0 auto;
    &.name {
      height: 90px;
    }
    &.role {
      height: 50px;
    }
    &.harbour {
      max-width: 50%;
      height: auto;
    }
  }
  .socials {
    font-size: 35px;
    margin-top: 25px;
    a {
      padding: 24px;
      color: #6eb2c1;
    }
  }
  .chevron {
    font-size: 40px;
    margin-top: 15px;
  }
}
</style>
