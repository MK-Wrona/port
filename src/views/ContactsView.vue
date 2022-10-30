<template>
  <div class="form_wrapper">
    <h2>Contact me</h2>
    <form class="form" name="form" id="form" novalidate @submit.prevent="sendEmail">
      <ul class="input_wrapper">
        <li>
          Name
          <input class="input" v-model="name" name="name"/>
          <label v-if="true" class="input_error">Check ur name, pal.</label>
        </li>
        <li>
          Email
          <input class="input" v-model="email" name="email"/>
        </li>
        <li>
          Message
          <textarea class="form_message" v-model="message" name="message"></textarea>
        </li>
      </ul>
      <input @click="sendEmail" type="submit" class="form_submit" value="Send">
    </form>
  </div>
</template>

<script>
import { useVuelidate } from '@vuelidate/core'
import { required, email } from '@vuelidate/validators'
import emailjs from 'emailjs-com';

const isEmail = value =>
    String(value).toLowerCase().match(
        /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/,
    )
const isName = value =>
    String(value).toLowerCase().match(/[A-Za-zА-Яа-яЁё]+(\s+[A-Za-zА-Яа-яЁё]+)?/)
export default {
  name: 'ContactUs',
  data() {
    return {
      name: '',
      email: '',
      message: ''
    }
  },
  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm('service_lbe459h', 'template_futry2f', document.querySelector('form'),
            'rYNd00-CYFAuNuUVq', {
              name: this.name,
              email: this.email,
              message: this.message
            })

      } catch(error) {
        console.log({error})
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  }
}
</script>

<style scoped>
.form {
  display: flex;
  flex-direction: column;
  width: 400px;
  padding-top: 80px;
}

.input_wrapper {
}

.form_wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.input {
  position: relative;
  border-radius: 10px;
}

.form_message {
  height: 100px;
}

.input_error {
  color: #3DDC84;
  position: absolute;
  left: 0px;
  font-size: small;
  bottom: 8px;
}

.form_submit {
  width: 30%;
  background-color: #3DDC84;
  border: none;
  font-weight: bold;
  border-radius: 10px;
  padding: 10px 10px 10px;
  cursor: pointer;
  align-self: end;
}

.form_submit:hover {
  color: white;
  cursor: pointer;
  background-color: #2F2F2F;
  border: 1px solid white;
  border-radius: 10px;
  padding: 9px 9px 9px;
  cursor: pointer;
}
</style>
