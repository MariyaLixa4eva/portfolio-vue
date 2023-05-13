<template>
<div class="navbar">
  <div class="nav-container">
    <div class="logo">
      <router-link to="/">
        <img alt="logo" src="../assets/logo.png" width="160" />
      </router-link>
    </div>
    
    <input class="checkbox" type="checkbox" name="" id="" />
    <div class="hamburger-lines">
      <span class="line line1"></span>
      <span class="line line2"></span>
      <span class="line line3"></span>
    </div>
    <div class="menu-items">
      <router-link to="/about">{{ $t("nav.about") }}</router-link>
      <router-link to="/project">{{ $t("nav.project") }}</router-link>
      <router-link to="/contact">{{ $t("nav.contact") }}</router-link>
    </div>
    <div class="locale">
      <LocaleSwitcher />
    </div>
  </div>
</div>
</template>
<script>
  import LocaleSwitcher from "@/components/LocaleSwitcher"
  export default {
    components: { LocaleSwitcher }
  }
</script>
<style scoped>
  .navbar {
    width: 100%;
    height:80px;
    font-size: 1.5rem;
    position: fixed;
    z-index: 5;
    background-color: var(--bg);
  }
  .nav-container {
    margin: 0 auto;
    max-width: 1200px;
    display: flex;
    justify-content: space-between;
  }
  .nav-container .checkbox {
    display: none;
  }
  .navbar .menu-items {
    margin-top: 15px;
  }
  .navbar .menu-items a {
    margin-right: 20px;
    padding: 15px;
  }
  .logo {
    margin-top: 5px;
    margin-left: 20px;
  }
  .locale {
    margin-top: 15px;
    margin-right: 20px;
  }
@media all and (max-width: 900px) {
  .nav-container {
    margin: auto;
    max-width: 1200px;
    display: block;
    position: relative;
  }
  .logo {
    position: absolute;
    left: 20px;
    top: 5px;
    z-index: 2;
    margin-top: 0px;
    margin-left: 0px;
  }
  .locale {
    position: absolute;
    right: 60px;
    top: 5px;
    z-index: 2;
  }
  .navbar .menu-items {
    height: 100vh;
    width: 100%;
    transform: translate(-150%);
    display: flex;
    flex-direction: column;
    justify-content: center;
    transition: transform 0.5s ease-in-out;
    text-align: center;
    position: relative;
    background-color: #0f152e;
    margin-top: 0px;
  }
  .navbar .menu-items a {
    margin-right: 0px;
  }
  .nav-container .checkbox {
    position: absolute;
    display: block;
    height: 32px;
    width: 32px;
    top: 20px;
    right: 20px;
    z-index: 5;
    opacity: 0;
    cursor: pointer;
  }
  .nav-container .hamburger-lines {
    display: block;
    height: 30px;
    width: 39px;
    position: absolute;
    top: 25px;
    right: 20px;
    z-index: 2;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .nav-container .hamburger-lines .line {
    display: block;
    height: 4px;
    width: 100%;
    border-radius: 10px;
    background: #4eb5d6;
  }
  .nav-container .hamburger-lines .line1 {
    transform-origin: 0% 0%;
    transition: transform 0.4s ease-in-out;
  }
  .nav-container .hamburger-lines .line2 {
    transition: transform 0.2s ease-in-out;
  }
  .nav-container .hamburger-lines .line3 {
    transform-origin: 0% 100%;
    transition: transform 0.4s ease-in-out;
  }
  .nav-container input[type="checkbox"]:checked ~ .menu-items {
    transform: translateX(0);
  }
  .nav-container input[type="checkbox"]:checked ~ .hamburger-lines .line1 {
    transform: rotate(45deg);
  }
  .nav-container input[type="checkbox"]:checked ~ .hamburger-lines .line2 {
    transform: scaleY(0);
  }
  .nav-container input[type="checkbox"]:checked ~ .hamburger-lines .line3 {
    transform: rotate(-45deg);
  }
}





 
</style>