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
              name="from_name"
              required
            />
          </div>
          <div class="form-group">
            <input
              type="email"
              class="name form-control text-center"
              placeholder="email"
              name="from_email"
              required
            />
          </div>
          <div class="form-group">
            <textarea
              class="form-control text-center"
              placeholder="Comment"
              rows="9"
              name="message_html"
              required
            ></textarea>
          </div>
          <button :disabled="enquirySent" type="submit">Submit</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import emailjs from "emailjs-com";

export default {
  name: "enquire",
  data() {
    return {
      enquirySent: false
    };
  },
  methods: {
    sendEmail(e) {
      emailjs
        .sendForm(
          process.env.VUE_APP_EMAIL_USER_ID,
          process.env.VUE_APP_TEMPLATE_ID,
          e.target,
          process.env.VUE_APP_EMAIL_USER_TOKEN
        )
        .then(() => {
          this.enquirySent = true;
          this.$toast.success(
            "Thank you for your enquiry, i'll get back to you as soon as I can!"
          );
        })
        .catch(() => {
          this.$toast.error(
            "Oops something went wrong, please try again later..."
          );
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
      margin-top: 25px;
      width: 140px;
      height: 45px;
      font-size: 15px;
      letter-spacing: 2.5px;
      font-weight: 500;
      color: #fff;
      background-color: #6eb4c7;
      border: 2px solid #6eb4c7;
      border-radius: 45px;
      box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
      transition: all 0.3s ease 0s;
      &:hover {
        background-color: #fff;
        box-shadow: 0px 15px 20px rgba(110, 180, 199, 0.4);
        color: #6eb4c7;
        cursor: pointer;
        transform: translateY(-7px);
      }
    }
  }
}
</style>