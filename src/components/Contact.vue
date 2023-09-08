<template>
  <div id="contact">
    <div class="container">
      <div class="contact-container">
        <div class="contact-main">
          <h3 class="title">Contact</h3>
          <p class="contact-description">
            I am always happy to hear from you. Feel free to contact us
            anytime and we will get back with a response as soon.
          </p>
          <div class="contact-items">
            <div class="flex-align">
              <a href="mailto:mdbayzidaman@gmail.com" class="contact-mail">
                <i class="fa-solid fa-envelope"></i>
                <span class="mail-address">mdbayzidaman@gmail.com</span>
              </a>
              <div @click="copyToClipboard" :class="copied? 'copied': ''" class="copy">
                <span class="material-symbols-outlined content_copy"> content_copy </span>   
                <span class="material-symbols-outlined done"> done </span>   
              </div>
            </div>
            <div class="contact-with-others">
              <a href="https://www.facebook.com/MdBayzidAman" target="_blank" class="contact-item">
                <i class="fa-brands fa-facebook"></i>
              </a>
              <a href="https://www.twitter.com/MdBayzidAman" target="_blank" class="contact-item">
                <i class="fa-brands fa-x-twitter"></i>
              </a>
              <a href="https://www.linkedin.com/in/MdBayzidAman" target="_blank" class="contact-item">
                <i class="fa-brands fa-linkedin"></i>
              </a>
              <a href="https://www.github.com/MdBayzidAman" target="_blank" class="contact-item">
                <i class="fa-brands fa-github"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";


const copied =ref(false)

const copyToClipboard =()=>{
  var mail= document.querySelector('.mail-address').innerHTML;
  console.log(navigator.clipboard.writeText(mail));
  
  copied.value = ref(true);

  setTimeout(() => {
    copied.value = !copied.value;
    console.log(copied.value);
  }, 1000);
}
</script>

<style scoped>
</style>
