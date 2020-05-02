<template>
  <div class="enquire">
    <div class="container">
      <div class="chevron jump text-center">
        <i class="fas fa-chevron-up"></i>
      </div>
      <p class="title text-center">Enquire</p>
      <div class="form">
        <form action="submit">
          <div class="form-group">
            <input type="text" class="name form-control text-center" placeholder="name" />
          </div>
          <div class="form-group">
            <input type="email" class="name form-control text-center" placeholder="email" />
          </div>
          <div class="form-group">
            <textarea class="form-control" rows="9"></textarea>
          </div>
          <button type="submit" class="btn btn-primary">Submit</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "enquire"
};
</script>

<style lang="scss" scoped>
.enquire {
  height: 100vh;
  font-family: "Comic Sans MS";
  color: #6eb4c7;
  .chevron {
    margin-top: 20px;
  }
  .title {
    font-size: 40px;
  }
  .form {
    padding: 50px 300px;
    background-color: #e0ebe8;
    .name {
      border: 2px solid #6eb4c7;
      border-radius: 50px;
      height: 50px;
      &::placeholder {
        color: #6eb4c7;
      }
    }
    textarea {
      border: 2px solid #6eb4c7;
      border-radius: 30px;
    }
  }
}
</style>