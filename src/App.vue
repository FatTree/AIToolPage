<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'

// import './assets/main.module.scss';

</script>

<template>
  <div class="container">
    <ul class="nav MaxW">
      <li class="nav__logos">
        <img class="logo" src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/logo.png?raw=true" alt="">
      </li>
      <li class="nav__links">
        <RouterLink to="/" class="nav__links__el TC-Body TC-Blob">首頁</RouterLink>
        <RouterLink to="/pricing" class="nav__links__el TC-Body TC-Blob">定價</RouterLink>
      </li>
      <li class="nav__links--rwd">
        <div class="material-icons">menu</div>
      </li>
    </ul>
    <RouterView />
    <Footer />
  </div>
</template>

<style lang="scss" scoped>
@import './assets/main.module.scss';
@import url('https://fonts.googleapis.com/icon?family=Material+Icons');
.container {
  // background-color: $Black100;
  color: $Black0;
  // min-width: 1180px;
}


.nav {
  border-bottom: 1px solid $Black0;
  display: flex;
  justify-content: space-between;
  padding: 28px 0;

  &__logos {
    > .logo {
      width: 245px;
      height: 40px;
    }
  }

  &__links {
    display: flex;

    &--rwd {
      display: none;
    }

    &__el {
      padding-left: 20px;
      color: $Black0;
    }
      
  }
}

@media screen and (max-width: 767px) {
  .container {
    margin: 0 12px
  }
	.nav {
    &__logos {
    > .logo {
      width: 174px;
      height: 24px;
    }
  }
    &__links {
      display: none;
      
      &--rwd {
        display: block;
      }
    }
  }
}

</style>
