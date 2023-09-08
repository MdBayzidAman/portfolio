<script setup>
import GreetView from '../components/GreetView.vue';
import Navbar from '../components/Navbar.vue';
import Project from '../components/Project.vue';
import Skill from '../components/Skill.vue';
import Splash from '../components/Splash.vue';
import Contact from '../components/Contact.vue';
import Service from '../components/Service.vue';


// theme
// const theme= {
//   primary: '#fff',
//   textColorPrimary: '#333'
// }

// document.documentElement.style.setProperty('--theme-primary', theme.primary);
// document.documentElement.style.setProperty('sadfs', theme.primary);
// document.documentElement.style.setProperty('--theme-color-primary', theme.textColorPrimary);

</script>

<template>
  <!-- splash -->
  <Splash />
  <!-- header -->
  <Navbar/>
  <!-- main content -->
  <main>
    <GreetView/>
    <!-- skills -->
    <Skill/>
    <!-- service -->
    <Service/>
    <!-- projects -->
    <Project/>
    <!-- contact -->
    <Contact/>
  </main>

  <!-- footer -->
  <footer>
    <div class="container">
      <p class="creator text-center">
        Made with ❤️ by Md Bayzid Aman
      </p>
    </div>
  </footer>
</template>
<style scoped>
footer{
  font-size: 20px;
  padding: 20px 0;
  background-color: var(--theme-secondary);
}
</style>
