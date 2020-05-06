<template>
  <div class="enquire">
    <div class="container">
      <div class="chevron jump text-center">
        <i class="fas fa-chevron-up"></i>
      </div>
      <p class="title text-center">Enquire</p>
      <div class="form text-center">
        <form action="submit" @submit.prevent="sendEmail">
          <div class="form-group">
            <input
              type="text"
              class="name form-control text-center"
              placeholder="name"
              name="user_name"
            />
          </div>
          <div class="form-group">
            <input
              type="email"
              class="name form-control text-center"
              placeholder="email"
              name="user_email"
            />
          </div>
          <div class="form-group">
            <textarea
              class="form-control text-center"
              placeholder="Comment"
              rows="9"
              name="message"
            ></textarea>
          </div>
          <button type="submit">Submit</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import emailjs from "emailjs-com";

export default {
  name: "enquire",
  methods: {
    sendEmail(e) {
      // let params = {
      //   name: "hello",
      //   email: "email@email.com",
      //   message: "Message"
      // };
      emailjs
        .sendForm(
          "6079",
          "template_cJ9DgMU9",
          e.target,
          "user_Ei1CA3QOgxcFGaZCxCE1M"
        )
        .then(result => {
          console.log("SUCCESS", result);
        })
        .catch(error => {
          console.log("ERROR", error);
        });
    }
  }
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
      &::placeholder {
        color: #6eb4c7;
        top: 40px;
      }
    }
    button {
      background-color: #70b4c2;
      border: none;
      color: #fff;
      font-size: 30px;
      border-radius: 50px;
      width: 250px;
      padding: 10px;
    }
  }
}
</style>