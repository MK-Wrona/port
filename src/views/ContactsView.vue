<template>
  <div class="form_wrapper">
    <h2>Contact me</h2>
    <form class="form" name="form" id="form" novalidate @submit.prevent="">
      <ul class="input_wrapper">
        <li>
          Name
          <input class="input" v-model="name" name="name"/>
          <label v-if="v$.name.$error" class="input_error">Check ur name, pal.</label>
        </li>
        <li>
          Email
          <input class="input" v-model="email" name="email"/>
          <label v-if="v$.name.$error" class="input_error">Weird email you have, mate.</label>
        </li>
        <li>
          Message
          <textarea style="resize: none;" class="form_message" v-model="message" name="message"></textarea>
        </li>
      </ul>
      <input @click="sendEmail" type="submit" class="form_submit" value="Send">
    </form>
    <div class="form_popup" id="form_popup">
      <div class="wrapper">
        <img src="/src/assets/close_icon.svg" class="popup_close" id="popup_close" @onclick="closePopup">
        <svg class="checkmark" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 52 52">
          <circle class="checkmark__circle" cx="26" cy="26" r="25" fill="none"/>
          <path class="checkmark__check" fill="none" d="M14.1 27.2l7.1 7.2 16.7-16.8"/>
        </svg>
        <p class="form_popup_text">I got your email!</p>
      </div>
    </div>
  </div>
</template>

<script>
import { useVuelidate } from '@vuelidate/core'
import { required, email } from '@vuelidate/validators'
import emailjs from 'emailjs-com'

const isEmail = value =>
    String(value).toLowerCase().match(
        /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/,
    )
const isName = value =>
    String(value).toLowerCase().match(/[A-Za-zА-Яа-яЁё]+(\s+[A-Za-zА-Яа-яЁё]+)?/)
export default {
  name: 'ContactUs',
  setup () {
    return { v$: useVuelidate() }
  },
  data () {
    return {
      name: '',
      email: '',
      message: '',
    }
  },
  sent: {
    type: Boolean,
    default: false,
  },
  validations () {
    return {
      name: {
        required,
        isName,
      },
      email: {
        required,
        isEmail,
      },
    }
  },
  methods: {
    showPopup () {
      document.querySelector('.form_popup').classList.add('popup_visibility')
    },
    closePopup () {
      document.querySelector('.popup_close').addEventListener('click', () => {
        document.querySelector('.form_popup').classList.remove('popup_visibility')
      })
    },
    sendEmail (e) {
      this.v$.$touch()
      if (this.v$.$errors.length === 0) {
        this.showPopup()
        emailjs.sendForm('service_lbe459h', 'template_futry2f', document.querySelector('form'),
            'rYNd00-CYFAuNuUVq', {
              name: this.name,
              email: this.email,
              message: this.message,
            })
        document.querySelector('.popup_close').addEventListener('click', () => {
          document.querySelector('.form_popup').classList.remove('popup_visibility')
        })
        this.v$.$reset()
      }
      else {
        console.log('Validation failed')
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  },
  computed: {},
}
</script>

<style scoped>


.wrapper {
  width: 100%;
  height: 100%;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: rgba(47, 47, 47, 0.99);
  font-size: 30px;
  font-weight: 700;
}

.checkmark__circle {
  stroke-dasharray: 166;
  stroke-dashoffset: 166;
  stroke-width: 2;
  stroke-miterlimit: 10;
  stroke: #3DDC84;
  fill: none;
  animation: stroke 0.6s cubic-bezier(0.65, 0, 0.45, 1) forwards
}

.checkmark {
  width: 56px;
  height: 56px;
  border-radius: 50%;
  display: block;
  stroke-width: 2;
  stroke: #fff;
  stroke-miterlimit: 10;
  margin: 10% auto;
  box-shadow: inset 0px 0px 0px #7ac142;
  animation: fill .4s ease-in-out .4s forwards, scale .3s ease-in-out .9s both
}

.checkmark__check {
  transform-origin: 50% 50%;
  stroke-dasharray: 48;
  stroke-dashoffset: 48;
  animation: stroke 0.3s cubic-bezier(0.65, 0, 0.45, 1) 0.8s forwards
}

@keyframes stroke {
  100% {
    stroke-dashoffset: 0
  }
}

@keyframes scale {
  0%, 100% {
    transform: none
  }
  50% {
    transform: scale3d(1.1, 1.1, 1)
  }
}

@keyframes fill {
  100% {
    box-shadow: inset 0px 0px 0px 30px #3DDC84
  }
}

.form {
  display: flex;
  flex-direction: column;
  width: 400px;
  padding-top: 80px;
}

.form_wrapper {
  position: relative;
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
  border-radius: 10px;
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
}

.form_popup {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50%;
  height: 100%;
  color: #3DDC84;
  visibility: hidden;
}

.popup_close {
  position: absolute;
  top: 8px;
  right: 8px;
  filter: invert(78%) sepia(84%) saturate(407%) hue-rotate(77deg) brightness(90%) contrast(91%);
  cursor: pointer;
}

.popup_visibility {
  visibility: visible;
}
@media screen and (max-width: 460px){
  .form {
    width: 100%;
    padding-top: 40px;
  }
  .form_submit {
    align-self: center;
    width:100%;
  }
}
@media screen and (max-width: 768px){
  .form_wrapper {
    padding-top:20px;
  }
}
</style>
