<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/Projects.vue'
import Footer from "./components/Footer.vue";
</script>

<template>
  <header>
    <nav class="wrapper">
      <div class="myself">
        <img src="/src/assets/logo_portfolio.svg" class="main_logo"/>
        <RouterLink to="/"><span class="header_link">Mara Krukovska</span></RouterLink>
      </div>
      <div>
        <RouterLink to="/contacts"><span class="header_link">Contacts</span></RouterLink>
        <RouterLink to="/about"><span class="header_link">About</span></RouterLink>
        <RouterLink to="/projects"><span class="header_link">Projects</span></RouterLink>
      </div>
    </nav>
  </header>
  <RouterView/>
  <Footer />
</template>

<style>
header {
  line-height: 1.5;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
  text-decoration: none;
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
  text-decoration: none;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid #3DDC84;
  text-decoration: none;
}

nav a:first-of-type {
  border: 0;
}
.myself {
  display: flex;
  justify-content: center;
}
.header_link {
  color: white;
  padding: 5px 10px 10px;
}
.header_link:hover {
  background-color: #2F2F2F;
  border-radius: 10px;
}
.main_logo {
  margin-top: -5px;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  .wrapper {
    width:100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
