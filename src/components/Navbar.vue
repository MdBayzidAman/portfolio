<template>
  <div @click="closeSideNave" class="overlay dn"></div>
  <header>
    <nav class="desktop-main-nav">
      <div class="container flex-align justify-side">
        <RouterLink to="/">
          <img alt="logo" class="logo" src="../assets/img/logo.png" />
        </RouterLink>
        <!-- <RouterLink to="/">Home</RouterLink> -->
        <ul class="menu-list flex-align justify-side">
          <!-- <li class="menu-item">
            <a class="menu-title" href="#about">About</a>
          </li> -->
          <li class="menu-item">
            <a class="menu-title" href="#skills">Skills</a>
          </li>
          <li class="menu-item">
            <a class="menu-title" href="#service">Service</a>
          </li>
          <li class="menu-item">
            <a class="menu-title" href="#contact">Contact</a>
          </li>
        </ul>
        <span @click="openSideNave" class="menu-bar dn"
          ><span class="material-symbols-outlined"> menu </span></span
        >
      </div>
    </nav>
    <nav class="mobile-side-nav">
      <div class="container">
        <span @click="closeSideNave" class="close-btn"
          ><span class="material-symbols-outlined"> close </span></span
        >
        <ul class="mobile-menu-list">
          <li class="menu-header">Menu</li>
          <li class="menu-item">
            <a href="#skills" class="menu-title">Skills</a>
          </li>
          <li class="menu-item">
            <a href="#service" class="menu-title">Service</a>
          </li>
          <li class="menu-item">
            <a href="#contact" class="menu-title">Contact</a>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script setup>
// sticky Navbar
window.addEventListener("scroll", function () {
  var navbar = document.querySelector(".desktop-main-nav");
  navbar.classList.toggle("sticky", window.scrollY > 400);
});

// open mobile side nav
const openSideNave = () => {
  document.querySelector(".mobile-side-nav").classList.add("active-side-nave");
  document.querySelector(".overlay").classList.add("active");
};
// close mobile side nav
const closeSideNave = () => {
  document
    .querySelector(".mobile-side-nav")
    .classList.remove("active-side-nave");
  document.querySelector(".overlay").classList.remove("active");
};
</script>

<style scoped></style>
